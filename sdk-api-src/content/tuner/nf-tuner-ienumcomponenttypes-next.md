---
UID: NF:tuner.IEnumComponentTypes.Next
title: IEnumComponentTypes::Next
author: windows-driver-content
description: The Next method retrieves the next n elements in the collection.
old-location: mstv\ienumcomponenttypes_next.htm
old-project: mstv
ms.assetid: 491e9237-38cd-4c12-b93b-eb398a49d742
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IEnumComponentTypes interface [Microsoft TV Technologies],Next method, IEnumComponentTypes.Next, IEnumComponentTypes::Next, IEnumComponentTypesNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumComponentTypes interface, mstv.ienumcomponenttypes_next, tuner/IEnumComponentTypes::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IEnumComponentTypes.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumComponentTypes::Next


## -description



The <b>Next</b> method retrieves the next <i>n</i> elements in the collection.




## -parameters




### -param celt [in]

The number of elements to retrieve.


### -param rgelt




### -param pceltFetched [out]

Receives the number of elements actually retrieved.


#### - pprgelt [out]

Address of an array of <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> interface pointers that will receive the returned <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> objects.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/ad7fb66d-6592-47ae-9a2f-4432d8aaaebb">IEnumComponentTypes Interface</a>
 

 

