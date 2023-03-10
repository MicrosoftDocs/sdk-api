---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync
title: IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync (efswrtinterop.h)
description: Request access to enterprise protected content for an identity. (IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync)
helpviewer_keywords: ["EDP.iprotectionpolicymanagerinterop2_requestaccesswithauditinginfoforwindowasync","IProtectionPolicyManagerInterop2 interface","RequestAccessWithAuditingInfoForWindowAsync method","IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync","IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync","RequestAccessWithAuditingInfoForWindowAsync","RequestAccessWithAuditingInfoForWindowAsync method","RequestAccessWithAuditingInfoForWindowAsync method","IProtectionPolicyManagerInterop2 interface","efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync"]
old-location: edp\iprotectionpolicymanagerinterop2_requestaccesswithauditinginfoforwindowasync.htm
tech.root: EDP
ms.assetid: 9C631272-BF69-4CA5-9664-45C6831C252F
ms.date: 12/05/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2_requestaccesswithauditinginfoforwindowasync, IProtectionPolicyManagerInterop2 interface,RequestAccessWithAuditingInfoForWindowAsync method, IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync, IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync, RequestAccessWithAuditingInfoForWindowAsync, RequestAccessWithAuditingInfoForWindowAsync method, RequestAccessWithAuditingInfoForWindowAsync method,IProtectionPolicyManagerInterop2 interface, efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync
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
 - IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync
 - efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync
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
 - IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync
---

# IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Request access to enterprise protected content for an identity.

## -parameters

### -param appWindow [in] [in]

A handle to the current window.

### -param sourceIdentity [in] [in]

The enterprise identity to which the content is protected. This is an email address or domain that is managed.

### -param targetIdentity [in] [in]

   The enterprise identity to which the content is being disclosed. This is an email address or domain.

### -param auditInfoUnk [in]

  An audit info object; an instance of <a href="/uwp/api/Windows.Security.EnterpriseData.ProtectionPolicyAuditInfo">ProtectionPolicyAuditInfo</a>.

### -param riid [iid_is] [out, retval]

  Reference to the identifier of the interface describing the type of interface pointer to return in <i>asyncOperation</i>.

### -param asyncOperation

An <a href="/uwp/api/Windows.Foundation.IAsyncOperation_TResult_">IAsyncOperation&lt;ProtectionPolicyEvaluationResult&gt;</a> with a value of the <a href="/uwp/api/windows.security.enterprisedata.protectionpolicyevaluationresult">ProtectionPolicyEvaluationResult</a> enumeration that is the result of the request.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/efswrtinterop/nn-efswrtinterop-iprotectionpolicymanagerinterop2">IProtectionPolicyManagerInterop2</a>
