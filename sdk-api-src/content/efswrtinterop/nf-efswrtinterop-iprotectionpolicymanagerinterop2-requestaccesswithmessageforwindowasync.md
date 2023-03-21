---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop2.RequestAccessWithMessageForWindowAsync
title: IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync (efswrtinterop.h)
description: Request access to enterprise protected content for an identity. (IProtectionPolicyManagerInterop2.RequestAccessWithMessageForWindowAsync)
helpviewer_keywords: ["EDP.iprotectionpolicymanagerinterop2_requestaccesswithmessageforwindowasync","IProtectionPolicyManagerInterop2 interface","RequestAccessWithMessageForWindowAsync method","IProtectionPolicyManagerInterop2.RequestAccessWithMessageForWindowAsync","IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync","RequestAccessWithMessageForWindowAsync","RequestAccessWithMessageForWindowAsync method","RequestAccessWithMessageForWindowAsync method","IProtectionPolicyManagerInterop2 interface","efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync"]
old-location: edp\iprotectionpolicymanagerinterop2_requestaccesswithmessageforwindowasync.htm
tech.root: EDP
ms.assetid: AC0E0ED0-C8C3-4058-B20D-4F8BB3D83A87
ms.date: 12/05/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2_requestaccesswithmessageforwindowasync, IProtectionPolicyManagerInterop2 interface,RequestAccessWithMessageForWindowAsync method, IProtectionPolicyManagerInterop2.RequestAccessWithMessageForWindowAsync, IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync, RequestAccessWithMessageForWindowAsync, RequestAccessWithMessageForWindowAsync method, RequestAccessWithMessageForWindowAsync method,IProtectionPolicyManagerInterop2 interface, efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync
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
 - IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync
 - efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync
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
 - IProtectionPolicyManagerInterop2.RequestAccessWithMessageForWindowAsync
---

# IProtectionPolicyManagerInterop2::RequestAccessWithMessageForWindowAsync


## -description

Request access to enterprise protected content for an identity.

## -parameters

### -param appWindow [in]

  A handle to the current window.

### -param sourceIdentity [in]

The enterprise identity to which the content is protected. This is an email address or domain that is managed.

### -param targetIdentity [in]

   The enterprise identity to which the content is being disclosed. This is an email address or domain.

### -param auditInfoUnk

  An audit info object; an instance of <a href="/uwp/api/Windows.Security.EnterpriseData.ProtectionPolicyAuditInfo">ProtectionPolicyAuditInfo</a>.

### -param messageFromApp [in]

  A message that will be displayed in the consent dialog so that the user can make a consent decision.

### -param riid [iid_is] [out, retval]

  Reference to the identifier of the interface describing the type of interface pointer to return in <i>asyncOperation</i>.

### -param asyncOperation

An <a href="/uwp/api/Windows.Foundation.IAsyncOperation_TResult_">IAsyncOperation&lt;ProtectionPolicyEvaluationResult&gt;</a> with a value of the <a href="/uwp/api/windows.security.enterprisedata.protectionpolicyevaluationresult">ProtectionPolicyEvaluationResult</a> enumeration that is the result of the request.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/efswrtinterop/nn-efswrtinterop-iprotectionpolicymanagerinterop2">IProtectionPolicyManagerInterop2</a>
