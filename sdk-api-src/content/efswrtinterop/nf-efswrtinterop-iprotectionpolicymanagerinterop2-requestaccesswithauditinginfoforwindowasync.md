---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync
title: IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync
author: windows-sdk-content
description: Request access to enterprise protected content for an identity.
old-location: edp\iprotectionpolicymanagerinterop2_requestaccesswithauditinginfoforwindowasync.htm
tech.root: EDP
ms.assetid: 9C631272-BF69-4CA5-9664-45C6831C252F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2_requestaccesswithauditinginfoforwindowasync, IProtectionPolicyManagerInterop2 interface,RequestAccessWithAuditingInfoForWindowAsync method, IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync, IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync, RequestAccessWithAuditingInfoForWindowAsync, RequestAccessWithAuditingInfoForWindowAsync method, RequestAccessWithAuditingInfoForWindowAsync method,IProtectionPolicyManagerInterop2 interface, efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessWithAuditingInfoForWindowAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IProtectionPolicyManagerInterop2.RequestAccessWithAuditingInfoForWindowAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

  An audit info object; an instance of <a href="https://msdn.microsoft.com/ibrary/windows/apps/windows.security.enterprisedata.protectionpolicyauditinfo.aspx">ProtectionPolicyAuditInfo</a>.


### -param riid [iid_is] [out, retval]

  Reference to the identifier of the interface describing the type of interface pointer to return in <i>asyncOperation</i>.


### -param asyncOperation

An <a href="https://msdn.microsoft.com/library/windows/apps/br206598.aspx">IAsyncOperation<ProtectionPolicyEvaluationResult></a> with a value of the <a href="https://msdn.microsoft.com/library/windows/apps/windows.security.enterprisedata.protectionpolicyevaluationresult.aspx">ProtectionPolicyEvaluationResult</a> enumeration that is the result of the request.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B4B5BD4B-8F5F-4C1A-902E-5FB7FF75616B">IProtectionPolicyManagerInterop2</a>
 

 

