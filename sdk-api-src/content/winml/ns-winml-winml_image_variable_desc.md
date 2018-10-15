---
UID: NS:winml.WINML_IMAGE_VARIABLE_DESC
title: WINML_IMAGE_VARIABLE_DESC
author: windows-sdk-content
description: Contains properties for the image variable description.
old-location: machinelearning\winml_image_variable_desc.htm
tech.root: MachineLearning
ms.assetid: 82EE6D9B-08C4-4128-BE8A-DF922AA7318E
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: MachineLearning.winml_image_variable_desc, PWINML_IMAGE_VARIABLE_DESC, PWINML_IMAGE_VARIABLE_DESC structure pointer, WINML_IMAGE_VARIABLE_DESC, WINML_IMAGE_VARIABLE_DESC structure, winml/PWINML_IMAGE_VARIABLE_DESC, winml/WINML_IMAGE_VARIABLE_DESC
ms.prod: windows
ms.technology: windows-sdk
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
 - WINML_IMAGE_VARIABLE_DESC
product: Windows
targetos: Windows
req.typenames: WINML_IMAGE_VARIABLE_DESC
req.redist: 
---

# WINML_IMAGE_VARIABLE_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains properties for the image variable description.


## -struct-fields




### -field ElementType

A <a href="https://msdn.microsoft.com/A8EB60A1-F769-460F-8C94-5D1DE3A1820F">WINML_TENSOR_DATA_TYPE</a> containing the element tensor data type.


### -field NumDimensions

The image variable dimension count.


### -field pShape

A pointer to the shape of the image variable.

