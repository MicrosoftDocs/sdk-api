---
UID: NF:wincrypt.CertDeleteCTLFromStore
title: CertDeleteCTLFromStore function
author: windows-sdk-content
description: The CertDeleteCTLFromStore function deletes the specified certificate trust list (CTL) context from a certificate store.
old-location: security\certdeletectlfromstore.htm
old-project: SecCrypto
ms.assetid: e24d3445-8929-463a-b771-1f25f4e999b5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CertDeleteCTLFromStore, CertDeleteCTLFromStore function [Security], _crypto2_certdeletectlfromstore, security.certdeletectlfromstore, wincrypt/CertDeleteCTLFromStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertDeleteCTLFromStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertDeleteCTLFromStore function


## -description


The <b>CertDeleteCTLFromStore</b> function deletes the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context from a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


## -parameters




### -param pCtlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure to be deleted.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. One possible error code is the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The store was opened read-only, and a delete operation is not allowed.

</td>
</tr>
</table>
 




## -remarks



All subsequent get or find operations for the CTL in this store fail. However, memory allocated for the CTL is not freed until all duplicated contexts have also been freed.

The <i>pCtlContext</i> parameter is always freed by this function by using 
<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>, even for an error.




## -see-also




<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>



<a href="cryptography_functions.htm">Certificate Trust List Functions</a>
 

 

