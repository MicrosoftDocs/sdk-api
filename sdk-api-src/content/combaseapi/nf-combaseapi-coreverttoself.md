---
UID: NF:combaseapi.CoRevertToSelf
title: CoRevertToSelf function (combaseapi.h)
description: Restores the authentication information on a thread of execution.
helpviewer_keywords: ["CoRevertToSelf","CoRevertToSelf function [COM]","_com_CoRevertToSelf","com.coreverttoself","combaseapi/CoRevertToSelf"]
old-location: com\coreverttoself.htm
tech.root: com
ms.assetid: 8061ddbe-ed21-47f7-9ac4-b3ec910ff89d
ms.date: 12/05/2018
ms.keywords: CoRevertToSelf, CoRevertToSelf function [COM], _com_CoRevertToSelf, com.coreverttoself, combaseapi/CoRevertToSelf
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoRevertToSelf
 - combaseapi/CoRevertToSelf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoRevertToSelf
---

# CoRevertToSelf function


## -description

Restores the authentication information on a thread of execution.



## -returns

This function supports the standard return values, including S_OK to indicate success.

## -remarks

<b>CoRevertToSelf</b>, which is a helper function that calls <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-reverttoself">IServerSecurity::RevertToSelf</a>, restores the authentication information on a thread to the authentication information on the thread before impersonation began.

<b>CoRevertToSelf</b> encapsulates the following common sequence of calls (error handling excluded):


``` syntax
    CoGetCallContext(IID_IServerSecurity, (void**)&pss);
    pss->RevertToSelf();
    pss->Release();

```


## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-reverttoself">IServerSecurity::RevertToSelf</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>
