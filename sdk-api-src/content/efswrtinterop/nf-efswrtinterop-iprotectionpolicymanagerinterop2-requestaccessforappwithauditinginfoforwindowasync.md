---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop2.RequestAccessForAppWithAuditingInfoForWindowAsync
title: IProtectionPolicyManagerInterop2::RequestAccessForAppWithAuditingInfoForWindowAsync (efswrtinterop.h)
description: Request access to enterprise-protected content for a specific target app.helpviewer_keywords: ["EDP.iprotectionpolicymanagerinterop2_requestaccessforappwithauditinginfoforwindowasync","IProtectionPolicyManagerInterop2 interface","RequestAccessForAppWithAuditingInfoForWindowAsync method","IProtectionPolicyManagerInterop2.RequestAccessForAppWithAuditingInfoForWindowAsync","IProtectionPolicyManagerInterop2::RequestAccessForAppWithAuditingInfoForWindowAsync","RequestAccessForAppWithAuditingInfoForWindowAsync","RequestAccessForAppWithAuditingInfoForWindowAsync method","RequestAccessForAppWithAuditingInfoForWindowAsync method","IProtectionPolicyManagerInterop2 interface","efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessForAppWithAuditingInfoForWindowAsync"]
old-location: edp\iprotectionpolicymanagerinterop2_requestaccessforappwithauditinginfoforwindowasync.htm
tech.root: EDP
ms.assetid: 91DEC69B-066E-427F-9C25-47B15EAD0D89
ms.date: 12/05/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2_requestaccessforappwithauditinginfoforwindowasync, IProtectionPolicyManagerInterop2 interface,RequestAccessForAppWithAuditingInfoForWindowAsync method, IProtectionPolicyManagerInterop2.RequestAccessForAppWithAuditingInfoForWindowAsync, IProtectionPolicyManagerInterop2::RequestAccessForAppWithAuditingInfoForWindowAsync, RequestAccessForAppWithAuditingInfoForWindowAsync, RequestAccessForAppWithAuditingInfoForWindowAsync method, RequestAccessForAppWithAuditingInfoForWindowAsync method,IProtectionPolicyManagerInterop2 interface, efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessForAppWithAuditingInfoForWindowAsync
f1_keywords:
- efswrtinterop/IProtectionPolicyManagerInterop2.RequestAccessForAppWithAuditingInfoForWindowAsync
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- efswrt.dll
api_name:
- IProtectionPolicyManagerInterop2.RequestAccessForAppWithAuditingInfoForWindowAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProtectionPolicyManagerInterop2::RequestAccessForAppWithAuditingInfoForWindowAsync


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


### -param auditInfoUnk [in]

  An audit info object; an instance of <a href="https://docs.microsoft.com/uwp/api/Windows.Security.EnterpriseData.ProtectionPolicyAuditInfo">ProtectionPolicyAuditInfo</a>.


### -param riid [iid_is] [out, retval]

  Reference to the identifier of the interface describing the type of interface pointer to return in <i>asyncOperation</i>.


### -param asyncOperation [out]

An <a href="https://docs.microsoft.com/uwp/api/Windows.Foundation.IAsyncOperation_TResult_">IAsyncOperation<ProtectionPolicyEvaluationResult></a> with a value of the <a href="https://docs.microsoft.com/uwp/api/windows.security.enterprisedata.protectionpolicyevaluationresult">ProtectionPolicyEvaluationResult</a> enumeration that is the result of the request.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/efswrtinterop/nn-efswrtinterop-iprotectionpolicymanagerinterop2">IProtectionPolicyManagerInterop2</a>
 

 

