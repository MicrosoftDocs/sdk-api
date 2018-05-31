---
UID: NF:objidl.IEnumUnknown.Skip
title: IEnumUnknown::Skip
author: windows-sdk-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: com\ienumunknown_skip.htm
old-project: com
ms.assetid: 6d73a119-0da8-4754-92c3-53f75d7be9e0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IEnumUnknown interface [COM],Skip method, IEnumUnknown.Skip, IEnumUnknown::Skip, Skip, Skip method [COM], Skip method [COM],IEnumUnknown interface, _com_ienumunknown_skip, com.ienumunknown_skip, objidlbase/IEnumUnknown::Skip
ms.prod: windows
ms.technology: windows-sdk
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
-	IEnumUnknown.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumUnknown::Skip


## -description


Skips over the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be skipped.


## -returns



If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a>
 

 

