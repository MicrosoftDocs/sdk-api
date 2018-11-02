---
UID: NF:objbase.IsEqualGUID
title: IsEqualGUID macro
author: windows-sdk-content
description: Determines whether two GUIDs are equal.
old-location: com\isequalguid.htm
tech.root: com
ms.assetid: 3580a0c4-e1f8-4bb7-ba66-c4702ecd11f1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IsEqualGUID, IsEqualGUID function [COM], _com_IsEqualGUID, com.isequalguid, winddi/IsEqualGUID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: objbase.h
req.include-header: GuidDef.h, Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - IsEqualGUID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsEqualGUID macro


## -description


Determines whether two GUIDs are equal.




## -parameters




### -param rguid1

TBD


### -param rguid2

TBD






#### - guid1 [in]

The first GUID.


#### - guid2 [in]

The second GUID.


## -remarks



<b>IsEqualGUID</b> is used by the <a href="https://msdn.microsoft.com/f55ae128-8667-45df-a93e-37812a3409b5">IsEqualCLSID</a> and <a href="https://msdn.microsoft.com/4753a5f2-78a0-4622-bf4c-fd19731fa9e4">IsEqualIID</a> functions.





## -see-also




<a href="https://msdn.microsoft.com/f55ae128-8667-45df-a93e-37812a3409b5">IsEqualCLSID</a>



<a href="https://msdn.microsoft.com/4753a5f2-78a0-4622-bf4c-fd19731fa9e4">IsEqualIID</a>
 

 

