---
UID: NF:tuner.IComponentTypes.EnumComponentTypes
title: IComponentTypes::EnumComponentTypes
author: windows-sdk-content
description: The EnumComponentTypes method returns an IEnumComponentTypes enumerator for all component types in the collection.
old-location: mstv\icomponenttypes_enumcomponenttypes.htm
old-project: mstv
ms.assetid: c070998c-4350-4630-80c0-e3db46154845
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EnumComponentTypes, EnumComponentTypes method [Microsoft TV Technologies], EnumComponentTypes method [Microsoft TV Technologies],IComponentTypes interface, IComponentTypes interface [Microsoft TV Technologies],EnumComponentTypes method, IComponentTypes.EnumComponentTypes, IComponentTypes::EnumComponentTypes, IComponentTypesEnumComponentTypes, mstv.icomponenttypes_enumcomponenttypes, tuner/IComponentTypes::EnumComponentTypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponentTypes.EnumComponentTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentTypes::EnumComponentTypes


## -description



The <b>EnumComponentTypes</b> method returns an <b>IEnumComponentTypes</b> enumerator for all component types in the collection.




## -parameters




### -param ppNewEnum [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/ad7fb66d-6592-47ae-9a2f-4432d8aaaebb">IEnumComponentTypes</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes Interface</a>
 

 

