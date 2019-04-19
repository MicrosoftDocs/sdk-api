---
UID: NS:winml.WINML_BINDING_DESC
title: WINML_BINDING_DESC (winml.h)
author: windows-sdk-content
description: Contains a description of the WinML binding.
old-location: machinelearning\winml_binding_desc.htm
tech.root: MachineLearning
ms.assetid: 928C2AD0-73DD-4ECA-AC54-36ED84A9E4E6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_binding_desc, PWINML_BINDING_DESC, PWINML_BINDING_DESC structure pointer, WINML_BINDING_DESC, WINML_BINDING_DESC structure, winml/PWINML_BINDING_DESC, winml/WINML_BINDING_DESC
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
 - WINML_BINDING_DESC
product: Windows
targetos: Windows
req.typenames: WINML_BINDING_DESC
req.redist: 
ms.custom: 19H1
---

# WINML_BINDING_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains a description of the WinML binding.


## -struct-fields




### -field Name

The name of the WinML binding.


### -field BindType

A <a href="https://msdn.microsoft.com/482DA039-2A91-4030-966A-6BFB2C9564C0">WINML_BINDING_TYPE</a> containing the type of the WinML binding.


### -field Tensor

A <a href="https://msdn.microsoft.com/A99A57DB-4602-4841-85FF-BC655CAB6C6F">WINML_TENSOR_BINDING_DESC</a> containing the description of the tensor binding.


### -field Sequence

A <a href="https://msdn.microsoft.com/6662327D-4BB9-40CB-869C-7BB1ADCB2D1C">WINML_SEQUENCE_BINDING_DESC</a> containing the description of the sequence binding.


### -field Map

A <a href="https://msdn.microsoft.com/3D9FE11A-6053-4F59-9488-08A92EB45A09">WINML_MAP_BINDING_DESC</a> containing the description of the map binding.


### -field Image

A <a href="https://msdn.microsoft.com/5FF6233A-8DB0-4868-925C-833B01CB9DE3">WINML_IMAGE_BINDING_DESC</a> containing the description of the image binding.


### -field Resource

A <a href="https://msdn.microsoft.com/14008D12-1F46-4629-A7A3-190EA2B4DC76">WINML_RESOURCE_BINDING_DESC</a> containing the description of the resource binding.

