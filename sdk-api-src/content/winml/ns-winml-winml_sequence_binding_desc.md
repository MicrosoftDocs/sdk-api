---
UID: NS:winml.WINML_SEQUENCE_BINDING_DESC
title: WINML_SEQUENCE_BINDING_DESC
author: windows-sdk-content
description: Contains description properties of the sequence binding.
old-location: machinelearning\winml_sequence_binding_desc.htm
tech.root: MachineLearning
ms.assetid: 6662327D-4BB9-40CB-869C-7BB1ADCB2D1C
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MachineLearning.winml_sequence_binding_desc, PWINML_SEQUENCE_BINDING_DESC, PWINML_SEQUENCE_BINDING_DESC structure pointer, WINML_SEQUENCE_BINDING_DESC, WINML_SEQUENCE_BINDING_DESC structure, winml/PWINML_SEQUENCE_BINDING_DESC, winml/WINML_SEQUENCE_BINDING_DESC
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
 - WINML_SEQUENCE_BINDING_DESC
product: Windows
targetos: Windows
req.typenames: WINML_SEQUENCE_BINDING_DESC
req.redist: 
---

# WINML_SEQUENCE_BINDING_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains description properties of the sequence binding.


## -struct-fields




### -field ElementCount

The element count in the sequence binding.


### -field ElementType

A <a href="https://msdn.microsoft.com/A8EB60A1-F769-460F-8C94-5D1DE3A1820F">WINML_TENSOR_DATA_TYPE</a> containing the element tensor data type.


### -field pStrings

A pointer to the element data of type string.


### -field pInts

The element data of type int.


### -field pFloats

A pointer to the element data of type float.


### -field pDoubles

A pointer to the element data of type double.

