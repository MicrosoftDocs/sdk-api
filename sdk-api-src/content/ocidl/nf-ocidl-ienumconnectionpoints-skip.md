---
UID: NF:ocidl.IEnumConnectionPoints.Skip
title: IEnumConnectionPoints::Skip
author: windows-sdk-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: com\ienumconnectionpoints_skip.htm
old-project: com
ms.assetid: 53080d41-c8b8-46ad-a5f1-6eceb497aa9b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IEnumConnectionPoints interface [COM],Skip method, IEnumConnectionPoints.Skip, IEnumConnectionPoints::Skip, Skip, Skip method [COM], Skip method [COM],IEnumConnectionPoints interface, _com_ienumconnectionpoints_skip, com.ienumconnectionpoints_skip, ocidl/IEnumConnectionPoints::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ocidl.h
api_name:
-	IEnumConnectionPoints.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumConnectionPoints::Skip


## -description


Skips over the specified number of items in the enumeration sequence.


## -parameters




### -param cConnections [in]

The number of items to be skipped.


## -returns



If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a>
 

 

