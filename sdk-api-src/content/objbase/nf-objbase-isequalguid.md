---
UID: NF:objbase.IsEqualGUID
title: IsEqualGUID macro (objbase.h)
author: windows-sdk-content
description: Determines whether two GUIDs are equal.
old-location: com\isequalguid.htm
tech.root: com
ms.assetid: 3580a0c4-e1f8-4bb7-ba66-c4702ecd11f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsEqualGUID, IsEqualGUID function [COM], _com_IsEqualGUID, com.isequalguid, winddi/IsEqualGUID
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
ms.custom: 19H1
---

# IsEqualGUID macro


## -description


Determines whether two GUIDs are equal.




## -parameters




### -param rguid1 [in]

The first GUID.


### -param rguid2 [in]

The second GUID.


## -remarks



<b>IsEqualGUID</b> is used by the <a href="https://docs.microsoft.com/windows/desktop/api/guiddef/nf-guiddef-isequalclsid">IsEqualCLSID</a> and <a href="https://docs.microsoft.com/windows/desktop/api/guiddef/nf-guiddef-isequaliid">IsEqualIID</a> functions.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/guiddef/nf-guiddef-isequalclsid">IsEqualCLSID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/guiddef/nf-guiddef-isequaliid">IsEqualIID</a>
 

 

