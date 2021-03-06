---
-api-id: T:Windows.AI.MachineLearning.Preview.LearningModelBindingPreview
-api-type: winrt class
---

<!-- Class syntax.
public class LearningModelBindingPreview : ILearningModelBindingPreview, IIterable<Object>>, IMapView<Object>
-->

# Windows.AI.MachineLearning.Preview.LearningModelBindingPreview

## -description
Represents the associations between model inputs and variable instances.

## -remarks

## -see-also

## -examples
 ```csharp
public void PrepareBinding(LearningModelPreview model, VideoFrame picture)
{
	ImageVariableDescriptorPreview inputImageDescription;
	List<ILearningModelVariableDescriptorPreview> inputFeatures = model.Description.InputFeatures.ToList();

    inputImageDescription =
         inputFeatures.FirstOrDefault(feature => feature.ModelFeatureKind == LearningModelFeatureKindPreview.Image)
         as ImageVariableDescriptorPreview;

    // Bind the image
    var binding = new LearningModelBindingPreview(model);
    binding.Bind(inputImageDescription, picture);
}
```

