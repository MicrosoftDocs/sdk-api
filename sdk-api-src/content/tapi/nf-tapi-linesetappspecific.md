---
UID: NF:tapi.lineSetAppSpecific
title: lineSetAppSpecific function
author: windows-sdk-content
description: The lineSetAppSpecific function enables an application to set the application-specific field of the specified call's call-information record.
old-location: tapi2\linesetappspecific.htm
tech.root: TAPI
ms.assetid: b7d51f62-3b19-4961-8d4c-a44dc8498f14
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "_tapi2_linesetappspecific, lineSetAppSpecific, lineSetAppSpecific function [TAPI 2.2], tapi/lineSetAppSpecific, tapi2.linesetappspecific"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - lineSetAppSpecific
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetAppSpecific function


## -description


The 
<b>lineSetAppSpecific</b> function enables an application to set the application-specific field of the specified call's call-information record.


## -parameters




### -param hCall

Handle to the call whose application-specific field needs to be set. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.


### -param dwAppSpecific

New content of the <b>dwAppSpecific</b> member for the call's 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure. This value is not interpreted by the Telephony API.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_NOTOWNER, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED.




## -remarks



The application-specific field in the 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> data structure that exists for each call is not interpreted by the Telephony API or any of its service providers. Its usage is entirely defined by the applications. The field can be read from the 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> record returned by 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>. However, 
<b>lineSetAppSpecific</b> must be used to set the field so that changes become visible to other applications. When this field is changed, all other applications with call handles are sent a LINE_CALLINFO message with an indication that the <b>dwAppSpecific</b> member has changed.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>
 

 

