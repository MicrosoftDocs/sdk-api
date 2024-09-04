---
UID: NF:tapi.TAPIERROR_FORMATMESSAGE
title: TAPIERROR_FORMATMESSAGE macro (tapi.h)
description: The TAPIERROR_FORMATMESSAGE macro generates an identifier for standard TAPI error codes that can be used in the FormatMessage function.
helpviewer_keywords: ["TAPIERROR_FORMATMESSAGE","TAPIERROR_FORMATMESSAGE macro [TAPI 2.2]","_tapi2_tapierror_formatmessage","tapi/TAPIERROR_FORMATMESSAGE","tapi2.tapierror_formatmessage"]
old-location: tapi2\tapierror_formatmessage.htm
tech.root: tapi3
ms.assetid: 95817592-467f-438e-ae81-b4c2fff42d1f
ms.date: 12/05/2018
ms.keywords: TAPIERROR_FORMATMESSAGE, TAPIERROR_FORMATMESSAGE macro [TAPI 2.2], _tapi2_tapierror_formatmessage, tapi/TAPIERROR_FORMATMESSAGE, tapi2.tapierror_formatmessage
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TAPIERROR_FORMATMESSAGE
 - tapi/TAPIERROR_FORMATMESSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - TAPIERROR_FORMATMESSAGE
---

# TAPIERROR_FORMATMESSAGE macro


## -description

The 
<b>TAPIERROR_FORMATMESSAGE</b> macro generates an identifier for standard TAPI error codes that can be used in the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function.

## -parameters

#### - ErrCode

TAPI error code.

## -remarks

This mechanism should be used only for displaying information on errors for which the application has no defined method of recovery (that is, unexpected or internal errors). In most cases (unlike the following simplified example), it is desirable to include additional text informing the user of actions the application takes (or the user should take) as a result of the unhandled error.

If the application gets an error result from any TAPI function, the error value can be passed to the 
<b>TAPIERROR_FORMATMESSAGE</b> macro, which generates the message identifier to be passed to <b>FormatMessage</b>. 


#### Examples

The following example uses <b>FormatMessage</b> to produce an error string that corresponds to a TAPI error code.


``` syntax
lResult = lineClose(hLine);

if (lResult < 0)
{
    FormatMessage(FORMAT_MESSAGE_FROM_HMODULE,
                  (LPCVOID)GetModuleHandle("TAPIUI.DLL"),
                  TAPIERROR_FORMATMESSAGE(lResult),
                  0,
                  (LPTSTR)pBuf,
                  BUFSIZE,
                  NULL);
    MessageBox(hWnd,pBuf,"TAPI ERROR",MB_OK);
}
```

