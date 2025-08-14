---
UID: NF:winbase.PowerCreateRequest
title: PowerCreateRequest function (winbase.h)
description: Creates a new power request object.
helpviewer_keywords: ["PowerCreateRequest","PowerCreateRequest function","base.powercreaterequest","winbase/PowerCreateRequest"]
old-location: base\powercreaterequest.htm
tech.root: base
ms.assetid: 2122bf00-9e6b-48ab-89b0-f53dd6804902
ms.date: 12/05/2018
ms.keywords: PowerCreateRequest, PowerCreateRequest function, base.powercreaterequest, winbase/PowerCreateRequest
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerCreateRequest
 - winbase/PowerCreateRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - PowerCreateRequest
---

# PowerCreateRequest function


## -description

Creates a new power request object.

## -parameters

### -param Context [in]

Points to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-reason_context">REASON_CONTEXT</a> structure that contains information about the power request.

## -returns

If the function succeeds, the return value is a handle to the power request object.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When the power request object is no longer needed, use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to free the handle and clean up the object.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-powerclearrequest">PowerClearRequest</a>



<a href="/windows/desktop/api/winbase/nf-winbase-powersetrequest">PowerSetRequest</a>