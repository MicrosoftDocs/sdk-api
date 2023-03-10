---
UID: NF:tapi.lineSetCallPrivilege
title: lineSetCallPrivilege function (tapi.h)
description: The lineSetCallPrivilege function sets the application's privilege to the specified privilege.
helpviewer_keywords: ["_tapi2_linesetcallprivilege","lineSetCallPrivilege","lineSetCallPrivilege function [TAPI 2.2]","tapi/lineSetCallPrivilege","tapi2.linesetcallprivilege"]
old-location: tapi2\linesetcallprivilege.htm
tech.root: tapi3
ms.assetid: a13d7cfd-3709-43fb-88b9-291928f2c0d8
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetcallprivilege, lineSetCallPrivilege, lineSetCallPrivilege function [TAPI 2.2], tapi/lineSetCallPrivilege, tapi2.linesetcallprivilege
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSetCallPrivilege
 - tapi/lineSetCallPrivilege
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetCallPrivilege
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
<a href="/windows/desktop/Tapi/linecallprivilege--constants">LINECALLPRIVILEGE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCALLPRIVILEGE, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

## -remarks

If the application is the sole owner of a non-idle call and can change its privilege to monitor, a LINEERR_INVALCALLSTATE error is returned. The application can also first drop the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a> to make the call transition to the <i>idle</i> state and then change its privilege.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>