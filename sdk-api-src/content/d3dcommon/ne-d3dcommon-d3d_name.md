---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D3D_NAME enumeration


## -description


Values that identify shader parameters that use system-value semantics.


## -enum-fields




### -field D3D_NAME_UNDEFINED

This parameter does not use a predefined system-value semantic.


### -field D3D_NAME_POSITION

This parameter contains position data.


### -field D3D_NAME_CLIP_DISTANCE

This parameter contains clip-distance data.


### -field D3D_NAME_CULL_DISTANCE

This parameter contains cull-distance data.


### -field D3D_NAME_RENDER_TARGET_ARRAY_INDEX

This parameter contains a render-target-array index.


### -field D3D_NAME_VIEWPORT_ARRAY_INDEX

This parameter contains a viewport-array index.


### -field D3D_NAME_VERTEX_ID

This parameter contains a vertex ID.


### -field D3D_NAME_PRIMITIVE_ID

This parameter contains a primitive ID.


### -field D3D_NAME_INSTANCE_ID

This parameter contains an instance ID.


### -field D3D_NAME_IS_FRONT_FACE

This parameter contains data that identifies whether or not the primitive faces the camera.


### -field D3D_NAME_SAMPLE_INDEX

This parameter contains a sampler-array index.


### -field D3D_NAME_FINAL_QUAD_EDGE_TESSFACTOR

This parameter contains one of four tessellation factors that correspond to the amount of parts that a quad patch is broken into along the given edge. This flag is used to tessellate a quad patch.


### -field D3D_NAME_FINAL_QUAD_INSIDE_TESSFACTOR

This parameter contains one of two tessellation factors that correspond to the amount of parts that a quad patch is broken into vertically and horizontally within the patch. This flag is used to tessellate a quad patch.


### -field D3D_NAME_FINAL_TRI_EDGE_TESSFACTOR

This parameter contains one of three tessellation factors that correspond to the amount of parts that a tri patch is broken into along the given edge. This flag is used to tessellate a tri patch.


### -field D3D_NAME_FINAL_TRI_INSIDE_TESSFACTOR

This parameter contains the tessellation factor that corresponds to the amount of parts that a tri patch is broken into within the patch. This flag is used to tessellate a tri patch.


### -field D3D_NAME_FINAL_LINE_DETAIL_TESSFACTOR

This parameter contains the tessellation factor that corresponds to the number of lines broken into within the patch. This flag is used to tessellate an isolines patch.


### -field D3D_NAME_FINAL_LINE_DENSITY_TESSFACTOR

This parameter contains the tessellation factor that corresponds to the number of lines that are created within the patch. This flag is used to tessellate an isolines patch.


### -field D3D_NAME_BARYCENTRICS

This parameter contains barycentric coordinate data.


### -field D3D_NAME_TARGET

This parameter contains render-target data.


### -field D3D_NAME_DEPTH

This parameter contains depth data.


### -field D3D_NAME_COVERAGE

This parameter contains alpha-coverage data.


### -field D3D_NAME_DEPTH_GREATER_EQUAL

This parameter signifies that the value is greater than or equal to a reference value. This flag is used to specify conservative depth for a pixel shader.


### -field D3D_NAME_DEPTH_LESS_EQUAL

This parameter signifies that the value is less than or equal to a reference value. This flag is used to specify conservative depth for a pixel shader.


### -field D3D_NAME_STENCIL_REF


            This parameter contains a stencil reference.
            See <a href="https://msdn.microsoft.com/6E336623-9746-4872-ADC1-C5489F53D7AE">Shader Specified Stencil Reference Value</a>.
          


### -field D3D_NAME_INNER_COVERAGE


            This parameter contains inner input coverage data.
            See <a href="https://msdn.microsoft.com/83F223C0-9282-4149-86CF-471B88829F76">Conservative Rasterization</a>.
          


### -field D3D10_NAME_UNDEFINED

This parameter does not use a predefined system-value semantic.


### -field D3D10_NAME_POSITION

This parameter contains position data.


### -field D3D10_NAME_CLIP_DISTANCE

This parameter contains clip-distance data.


### -field D3D10_NAME_CULL_DISTANCE

This parameter contains cull-distance data.


### -field D3D10_NAME_RENDER_TARGET_ARRAY_INDEX

This parameter contains a render-target-array index.


### -field D3D10_NAME_VIEWPORT_ARRAY_INDEX

This parameter contains a viewport-array index.


### -field D3D10_NAME_VERTEX_ID

This parameter contains a vertex ID.


### -field D3D10_NAME_PRIMITIVE_ID

This parameter contains a primitive ID.


### -field D3D10_NAME_INSTANCE_ID

This parameter contains a instance ID.


### -field D3D10_NAME_IS_FRONT_FACE

This parameter contains data that identifies whether or not the primitive faces the camera.


### -field D3D10_NAME_SAMPLE_INDEX

This parameter contains a sampler-array index.


### -field D3D10_NAME_TARGET

This parameter contains render-target data.


### -field D3D10_NAME_DEPTH

This parameter contains depth data.


### -field D3D10_NAME_COVERAGE

This parameter contains alpha-coverage data.


### -field D3D11_NAME_FINAL_QUAD_EDGE_TESSFACTOR

This parameter contains one of four tessellation factors that correspond to the amount of parts that a quad patch is broken into along the given edge. This flag is used to tessellate a quad patch.


### -field D3D11_NAME_FINAL_QUAD_INSIDE_TESSFACTOR

This parameter contains one of two tessellation factors that correspond to the amount of parts that a quad patch is broken into vertically and horizontally within the patch. This flag is used to tessellate a quad patch.


### -field D3D11_NAME_FINAL_TRI_EDGE_TESSFACTOR

This parameter contains one of three tessellation factors that correspond to the amount of parts that a tri patch is broken into along the given edge. This flag is used to tessellate a tri patch.


### -field D3D11_NAME_FINAL_TRI_INSIDE_TESSFACTOR

This parameter contains the tessellation factor that corresponds to the amount of parts that a tri patch is broken into within the patch. This flag is used to tessellate a tri patch.


### -field D3D11_NAME_FINAL_LINE_DETAIL_TESSFACTOR

This parameter contains the tessellation factor that corresponds to the amount of lines broken into within the patch. This flag is used to tessellate an isolines patch.


### -field D3D11_NAME_FINAL_LINE_DENSITY_TESSFACTOR

This parameter contains the tessellation factor that corresponds to the amount of lines that are created within the patch. This flag is used to tessellate an isolines patch.


### -field D3D11_NAME_DEPTH_GREATER_EQUAL

This parameter signifies that the value is greater than or equal to a reference value. This flag is used to specify conservative depth for a pixel shader.


### -field D3D11_NAME_DEPTH_LESS_EQUAL

This parameter signifies that the value is less than or equal to a reference value. This flag is used to specify conservative depth for a pixel shader.


### -field D3D11_NAME_STENCIL_REF


            This parameter contains a stencil reference.
            See <a href="https://msdn.microsoft.com/6E336623-9746-4872-ADC1-C5489F53D7AE">Shader Specified Stencil Reference Value</a>.
          


### -field D3D11_NAME_INNER_COVERAGE


            This parameter contains inner input coverage data.
            See <a href="https://msdn.microsoft.com/83F223C0-9282-4149-86CF-471B88829F76">Conservative Rasterization</a>.
          


### -field D3D12_NAME_BARYCENTRICS


            This parameter contains barycentric coordinate data.
          


## -remarks




          The <b>D3D_NAME</b> values identify shader parameters that have <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">predefined system-value</a> semantics. These values are used in a shader-signature description. For more information about shader-signature description, see <a href="https://msdn.microsoft.com/3aed2f5f-1cfa-4224-bfcc-7d015e6a2cc0">D3D11_SIGNATURE_PARAMETER_DESC</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>



<a href="https://msdn.microsoft.com/3aed2f5f-1cfa-4224-bfcc-7d015e6a2cc0">D3D11_SIGNATURE_PARAMETER_DESC</a>
 

 

