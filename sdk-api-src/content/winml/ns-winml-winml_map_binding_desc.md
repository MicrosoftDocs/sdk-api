---
UID: NS:winml.WINML_MAP_BINDING_DESC
title: WINML_MAP_BINDING_DESC
author: windows-sdk-content
description: Contains properties for the binding of type map.
old-location: machinelearning\winml_map_binding_desc.htm
old-project: MachineLearning
ms.assetid: 3D9FE11A-6053-4F59-9488-08A92EB45A09
ms.author: windowssdkdev
ms.date: 03/07/2018
ms.keywords: MachineLearning.winml_map_binding_desc, PWINML_MAP_BINDING_DESC, PWINML_MAP_BINDING_DESC structure pointer, WINML_MAP_BINDING_DESC, WINML_MAP_BINDING_DESC structure, winml/PWINML_MAP_BINDING_DESC, winml/WINML_MAP_BINDING_DESC
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
req.typenames: WINML_MAP_BINDING_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winml.h
api_name:
-	WINML_MAP_BINDING_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WINML_MAP_BINDING_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains properties for the binding of type map.


## -struct-fields




### -field ElementCount

Element count in the map binding. 


### -field KeyType

A <a href="https://msdn.microsoft.com/A8EB60A1-F769-460F-8C94-5D1DE3A1820F">WINML_TENSOR_DATA_TYPE</a> containing the key element tensor data type.


### -field pStringKeys

A pointer to the key data of type string.


### -field pIntKeys

A pointer to the key data of type int.


### -field Fields

A <a href="https://msdn.microsoft.com/A8EB60A1-F769-460F-8C94-5D1DE3A1820F">WINML_TENSOR_DATA_TYPE</a> containing the field element tensor data type. 


### -field pStringFields

A pointer to the field data of type string.


### -field pIntFields

A pointer to the field data of type int.


### -field pFloatFields

A Pointer to the field data of type string.


### -field pDoubleFields

A pointer to the field data of type int.

