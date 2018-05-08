---
UID: NC:ntsecpkg.LSA_CANCEL_NOTIFICATION
title: LSA_CANCEL_NOTIFICATION
author: windows-driver-content
description: The CancelNotification function cancels a previously registered notification.
old-location: security\cancelnotification.htm
old-project: SecAuthN
ms.assetid: b7333318-ee17-4cc2-9382-2d4871ddee78
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CancelNotification, CancelNotification function [Security], LSA_CANCEL_NOTIFICATION, _ssp_cancelnotification, ntsecpkg/CancelNotification, security.cancelnotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	CancelNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_CANCEL_NOTIFICATION callback function


## -description


The <b>CancelNotification</b> function cancels a previously registered notification.


## -parameters




### -param NotifyHandle [in]

Handle returned by a previous call to 
<a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a>.


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
<a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a> function to register a notification.

A pointer to the <b>CancelNotification</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

