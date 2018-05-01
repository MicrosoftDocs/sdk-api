---
UID: NF:objidl.IEnumMoniker.Skip
title: IEnumMoniker::Skip method
author: windows-driver-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: com\ienummoniker_skip.htm
old-project: com
ms.assetid: 90df5bc4-6bb0-44bf-b675-d4a93d4680ce
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IEnumMoniker, IEnumMoniker interface [COM], Skip method, IEnumMoniker::Skip, Skip method [COM], Skip method [COM], IEnumMoniker interface, Skip,IEnumMoniker.Skip, _ole_ienummoniker_skip, com.ienummoniker_skip, objidl/IEnumMoniker::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
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
-	ObjIdl.h
api_name:
-	IEnumMoniker.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumMoniker::Skip method


## -description


Skips over the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be skipped.


## -returns



If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a>
 

 

