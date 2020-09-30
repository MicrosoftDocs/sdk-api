---
UID: NF:sas.SendSAS
title: SendSAS function (sas.h)
description: Simulates a secure attention sequence (SAS).
helpviewer_keywords: ["SendSAS","SendSAS function [Security]","sas/SendSAS","security.sendsas"]
old-location: security\sendsas.htm
tech.root: security
ms.assetid: da5d0915-dc41-4b63-a500-a0bec3f19a65
ms.date: 12/05/2018
ms.keywords: SendSAS, SendSAS function [Security], sas/SendSAS, security.sendsas
req.header: sas.h
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
req.lib: Sas.lib
req.dll: Sas.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SendSAS
 - sas/SendSAS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sas.dll
api_name:
 - SendSAS
---

# SendSAS function


## -description

Simulates a <a href="/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS).

## -parameters

### -param AsUser [in]

<b>TRUE</b> if the caller is running as the current user; otherwise, <b>FALSE</b>.

## -remarks

To successfully call the <b>SendSAS</b> function, an application must either be running as a service or have the <b>uiAccess</b> attribute of the <b>requestedExecutionLevel</b> element set to "true" in its application manifest. If an application is not running as a service, it must be running as either the current user or the LocalSystem account to call <b>SendSAS</b>. In addition, if an application is not running as a service, <a href="/windows/desktop/SecAuthZ/user-account-control">User Account Control</a> must be turned on to call <b>SendSAS</b>. 

<div class="alert"><b>Important</b>  Applications with the <b>uiAccess</b> attribute set to "true" must be signed by using <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85)">Authenticode</a>. In addition, the application must reside in a protected location in the file system. Currently, there are two allowable protected locations:<dl>
<dd><b>\Program Files\</b></dd>
<dd><b>\windows\system32\</b></dd>
</dl>
</div>
<div> </div>
The local security policy of a computer must be configured to allow services and applications to simulate a SAS. To configure the policy, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in. The GPE settings that control delegation are in the following location:

<b>Computer Configuration | Administrative Templates | Windows Components | Windows Logon Options | Disable or enable software Secure Attention Sequence</b>

A service can impersonate the token of another process that calls that service. In this case, a call to the <b>SendSAS</b> function by that service simulates a SAS on the session associated with the impersonated token.

<b>Windows Server 2008 and Windows Vista:  </b>Sas.dll is not available natively. You must download the Windows 7 version of the Microsoft Windows Software Development Kit (SDK)  to use this function. In addition, an application must refer to Sas.dll to call this function.