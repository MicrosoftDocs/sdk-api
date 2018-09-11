---
UID: NF:tapi.lineSetCallPrivilege
title: lineSetCallPrivilege function
author: windows-sdk-content
description: The lineSetCallPrivilege function sets the application's privilege to the specified privilege.
old-location: tapi2\linesetcallprivilege.htm
tech.root: tapi
ms.assetid: a13d7cfd-3709-43fb-88b9-291928f2c0d8
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linesetcallprivilege, lineSetCallPrivilege, lineSetCallPrivilege function [TAPI 2.2], tapi/lineSetCallPrivilege, tapi2.linesetcallprivilege"
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
 - lineSetCallPrivilege
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetCallPrivilege function


## -description


The 
<b>lineSetCallPrivilege</b> function sets the application's privilege to the specified privilege.


## -parameters




### -param hCall

Handle to the call whose privilege is to be set. The call state of <i>hCall</i> can be any state.


### -param dwCallPrivilege

Required privilege for the specified call. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/a58b7e9e-696e-4421-9b31-1ba8afe6e03b">LINECALLPRIVILEGE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCALLPRIVILEGE, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -remarks



If the application is the sole owner of a non-idle call and can change its privilege to monitor, a LINEERR_INVALCALLSTATE error is returned. The application can also first drop the call using 
<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a> to make the call transition to the <i>idle</i> state and then change its privilege.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>
 

 

