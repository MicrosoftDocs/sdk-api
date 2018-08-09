---
UID: NF:tapi.tapiRequestDrop
title: tapiRequestDrop function
author: windows-sdk-content
description: Closes a call request made by a previous call to tapiRequestMediaCall.
old-location: tapi2\tapirequestdrop.htm
old-project: tapi
ms.assetid: 57fe47c8-5a03-4c31-8008-0ebca88a840c
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: tapi/tapiRequestDrop, tapi2.tapirequestdrop, tapiRequestDrop, tapiRequestDrop function [TAPI 2.2]
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - tapiRequestDrop
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# tapiRequestDrop function


## -description


Closes a call request made by a previous call to <a href="https://msdn.microsoft.com/51db5bf7-debc-4a76-ba55-283fb30ba3ae">tapiRequestMediaCall</a>.
<div class="alert"><b>Note</b>  The tapiRequestDrop function is nonfunctional and obsolete for all classes of Windows-based applications. It should not be used.</div><div> </div>

## -parameters




### -param hwnd

TBD


### -param wRequestID

Pointer to a 32-bit integer value that contains the ID of the call request.


#### - hWnd

Handle to the Windows process that issued this request.


## -returns



The function is obsolete and will always return an error code. 




## -see-also




<a href="https://msdn.microsoft.com/43ca86b0-0107-4937-b15a-47916e144527">Assisted Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

