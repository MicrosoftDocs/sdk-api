---
UID: NC:ntsecpkg.LSA_CANCEL_NOTIFICATION
title: LSA_CANCEL_NOTIFICATION (ntsecpkg.h)
description: The CancelNotification function cancels a previously registered notification.
helpviewer_keywords: ["CancelNotification","CancelNotification callback function [Security]","LSA_CANCEL_NOTIFICATION","LSA_CANCEL_NOTIFICATION callback","_ssp_cancelnotification","ntsecpkg/CancelNotification","security.cancelnotification"]
old-location: security\cancelnotification.htm
tech.root: security
ms.assetid: b7333318-ee17-4cc2-9382-2d4871ddee78
ms.date: 12/05/2018
ms.keywords: CancelNotification, CancelNotification callback function [Security], LSA_CANCEL_NOTIFICATION, LSA_CANCEL_NOTIFICATION callback, _ssp_cancelnotification, ntsecpkg/CancelNotification, security.cancelnotification
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - LSA_CANCEL_NOTIFICATION
 - ntsecpkg/LSA_CANCEL_NOTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - CancelNotification
---

# LSA_CANCEL_NOTIFICATION callback function


## -description

The <b>CancelNotification</b> function cancels a previously registered notification.

## -parameters

### -param NotifyHandle [in]

Handle returned by a previous call to 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_register_notification">RegisterNotification</a>.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed. The following table lists a common reason for failure and the error code that the function returns.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>NotifyHandle</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

Use the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_register_notification">RegisterNotification</a> function to register a notification.

A pointer to the <b>CancelNotification</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_register_notification">RegisterNotification</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>