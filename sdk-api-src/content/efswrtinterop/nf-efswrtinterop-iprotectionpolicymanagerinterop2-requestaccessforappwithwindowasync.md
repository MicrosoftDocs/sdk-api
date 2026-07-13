---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop2.RequestAccessForAppWithWindowAsync
title: IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync (efswrtinterop.h)
description: Request access to enterprise-protected content for a specific target app. (IProtectionPolicyManagerInterop2.RequestAccessForAppWithWindowAsync)
helpviewer_keywords: ["EDP.iprotectionpolicymanagerinterop2_requestaccessforappwithwindowasync","IProtectionPolicyManagerInterop2 interface","RequestAccessForAppWithWindowAsync method","IProtectionPolicyManagerInterop2.RequestAccessForAppWithWindowAsync","IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync","RequestAccessForAppWithWindowAsync","RequestAccessForAppWithWindowAsync method","RequestAccessForAppWithWindowAsync method","IProtectionPolicyManagerInterop2 interface","efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync"]
old-location: edp\iprotectionpolicymanagerinterop2_requestaccessforappwithwindowasync.htm
tech.root: EDP
ms.assetid: 41F0047C-6442-4157-B710-E0DAF61DE44A
ms.date: 12/05/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2_requestaccessforappwithwindowasync, IProtectionPolicyManagerInterop2 interface,RequestAccessForAppWithWindowAsync method, IProtectionPolicyManagerInterop2.RequestAccessForAppWithWindowAsync, IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync, RequestAccessForAppWithWindowAsync, RequestAccessForAppWithWindowAsync method, RequestAccessForAppWithWindowAsync method,IProtectionPolicyManagerInterop2 interface, efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync
req.header: efswrtinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Efswrtinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Efswrt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync
 - efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - efswrt.dll
api_name:
 - IProtectionPolicyManagerInterop2.RequestAccessForAppWithWindowAsync
---

# IProtectionPolicyManagerInterop2::RequestAccessForAppWithWindowAsync


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Request access to enterprise-protected content for a specific target app.

## -parameters

### -param appWindow [in]

  A handle to the current window.

### -param sourceIdentity [in]

  The enterprise identity to which the content is protected. This is an email address or domain that is managed.

### -param appPackageFamilyName [in]

  The enterprise identity to which the content is being disclosed. This is an email address or domain.

### -param riid [iid_is] [out, retval]

  Reference to the identifier of the interface describing the type of interface pointer to return in <i>asyncOperation</i>.

### -param asyncOperation

An <a href="/uwp/api/Windows.Foundation.IAsyncOperation_TResult_">IAsyncOperation&lt;ProtectionPolicyEvaluationResult&gt;</a> with a value of the <a href="/uwp/api/windows.security.enterprisedata.protectionpolicyevaluationresult">ProtectionPolicyEvaluationResult</a> enumeration that is the result of the request.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/efswrtinterop/nn-efswrtinterop-iprotectionpolicymanagerinterop2">IProtectionPolicyManagerInterop2</a>
