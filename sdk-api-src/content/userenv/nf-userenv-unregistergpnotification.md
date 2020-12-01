---
UID: NF:userenv.UnregisterGPNotification
title: UnregisterGPNotification function (userenv.h)
description: The UnregisterGPNotification function unregisters the specified policy-notification handle from receiving policy change notifications.
helpviewer_keywords: ["UnregisterGPNotification","UnregisterGPNotification function [Group Policy]","_win32_unregistergpnotification","policy.unregistergpnotification","userenv/UnregisterGPNotification"]
old-location: policy\unregistergpnotification.htm
tech.root: Policy
ms.assetid: 39ac1361-0160-44e3-8b99-ff50978cc425
ms.date: 12/05/2018
ms.keywords: UnregisterGPNotification, UnregisterGPNotification function [Group Policy], _win32_unregistergpnotification, policy.unregistergpnotification, userenv/UnregisterGPNotification
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnregisterGPNotification
 - userenv/UnregisterGPNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - UnregisterGPNotification
---

# UnregisterGPNotification function


## -description

The 
    <b>UnregisterGPNotification</b> function unregisters the specified policy-notification handle from receiving policy change notifications.

## -parameters

### -param hEvent [in]

Policy-notification handle passed to the 
<a href="/windows/desktop/api/userenv/nf-userenv-registergpnotification">RegisterGPNotification</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller must call the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle when it is no longer needed.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/userenv/nf-userenv-registergpnotification">RegisterGPNotification</a>