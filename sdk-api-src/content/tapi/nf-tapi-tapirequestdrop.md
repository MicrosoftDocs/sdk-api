---
UID: NF:tapi.tapiRequestDrop
title: tapiRequestDrop function (tapi.h)
author: windows-sdk-content
description: Closes a call request made by a previous call to tapiRequestMediaCall.
old-location: tapi2\tapirequestdrop.htm
tech.root: Tapi
ms.assetid: 57fe47c8-5a03-4c31-8008-0ebca88a840c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: tapi/tapiRequestDrop, tapi2.tapirequestdrop, tapiRequestDrop, tapiRequestDrop function [TAPI 2.2]
ms.topic: function
f1_keywords: 
 - "tapi/tapiRequestDrop"
dev_langs:
 - c++
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - tapiRequestDrop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# tapiRequestDrop function


## -description


Closes a call request made by a previous call to <a href="https://docs.microsoft.com/windows/desktop/Tapi/tapirequestmediacall">tapiRequestMediaCall</a>.
<div class="alert"><b>Note</b>  The tapiRequestDrop function is nonfunctional and obsolete for all classes of Windows-based applications. It should not be used.</div><div> </div>

## -parameters




### -param hwnd

Handle to the Windows process that issued this request.


### -param wRequestID

Pointer to a 32-bit integer value that contains the ID of the call request.


## -returns



The function is obsolete and will always return an error code. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/assisted-telephony-services-reference">Assisted Telephony Services Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
 

 

