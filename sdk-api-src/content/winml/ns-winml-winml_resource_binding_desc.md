---
UID: NS:winml.WINML_RESOURCE_BINDING_DESC
title: WINML_RESOURCE_BINDING_DESC
author: windows-sdk-content
description: Contains description properties of the resource binding.
old-location: machinelearning\winml_resource_binding_desc.htm
tech.root: MachineLearning
ms.assetid: 14008D12-1F46-4629-A7A3-190EA2B4DC76
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MachineLearning.winml_resource_binding_desc, PWINML_RESOURCE_BINDING_DESC, PWINML_RESOURCE_BINDING_DESC structure pointer, WINML_RESOURCE_BINDING_DESC, WINML_RESOURCE_BINDING_DESC structure, winml/PWINML_RESOURCE_BINDING_DESC, winml/WINML_RESOURCE_BINDING_DESC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winml.h
api_name:
 - WINML_RESOURCE_BINDING_DESC
product: Windows
targetos: Windows
req.typenames: WINML_RESOURCE_BINDING_DESC
req.redist: 
---

# WINML_RESOURCE_BINDING_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains description properties of the resource binding.


## -struct-fields




### -field ElementType

A <a href="https://msdn.microsoft.com/A8EB60A1-F769-460F-8C94-5D1DE3A1820F">WINML_TENSOR_DATA_TYPE</a> containing the element tensor data type.


### -field NumDimensions

The resource dimension count.


### -field pShape

A pointer to the shape of the resource.


### -field pResource

A pointer to an <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> describing the D3D12 resource.

