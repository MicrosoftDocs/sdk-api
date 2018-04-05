---
UID: NF:objidl.IEnumString.Skip
title: IEnumString::Skip method
author: windows-driver-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: com\ienumstring_skip.htm
old-project: com
ms.assetid: 8c1cd7b4-ec68-4b60-9f1e-ed01674f7f8c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IEnumString, IEnumString interface [COM], Skip method, IEnumString::Skip, Skip method [COM], Skip method [COM], IEnumString interface, Skip,IEnumString.Skip, _com_ienumstring_skip, com.ienumstring_skip, objidlbase/IEnumString::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IEnumString.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IEnumString::Skip method


## -description


Skips over the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be skipped.


## -returns



If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>
 

 

