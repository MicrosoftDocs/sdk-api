---
UID: NF:tuner.IEnumComponentTypes.Clone
title: IEnumComponentTypes::Clone
author: windows-sdk-content
description: The Clone method creates a new copy of the collection and all its sub-objects.
old-location: mstv\ienumcomponenttypes_clone.htm
old-project: mstv
ms.assetid: 777c7302-5b5b-4263-ad9e-3d1bff5328fc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IEnumComponentTypes interface, IEnumComponentTypes interface [Microsoft TV Technologies],Clone method, IEnumComponentTypes.Clone, IEnumComponentTypes::Clone, IEnumComponentTypesClone, mstv.ienumcomponenttypes_clone, tuner/IEnumComponentTypes::Clone
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
 - IEnumComponentTypes.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumComponentTypes::Clone


## -description



The <b>Clone</b> method creates a new copy of the collection and all its sub-objects.




## -parameters




### -param ppEnum [out]

Address of an <b>IEnumComponentTypes</b> interface pointer that will be set to the returned collection object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/ad7fb66d-6592-47ae-9a2f-4432d8aaaebb">IEnumComponentTypes Interface</a>
 

 

