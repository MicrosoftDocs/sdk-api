---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop2.RequestAccessForAppWithMessageForWindowAsync
title: IProtectionPolicyManagerInterop2::RequestAccessForAppWithMessageForWindowAsync
author: windows-sdk-content
description: Request access to enterprise-protected content for a specific target app.
old-location: edp\iprotectionpolicymanagerinterop2_requestaccessforappwithmessageforwindowasync.htm
old-project: EDP
ms.assetid: D78D0095-826A-4E6F-9420-873382A76B87
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EDP.iprotectionpolicymanagerinterop2_requestaccessforappwithmessageforwindowasync, IProtectionPolicyManagerInterop2 interface,RequestAccessForAppWithMessageForWindowAsync method, IProtectionPolicyManagerInterop2.RequestAccessForAppWithMessageForWindowAsync, IProtectionPolicyManagerInterop2::RequestAccessForAppWithMessageForWindowAsync, RequestAccessForAppWithMessageForWindowAsync, RequestAccessForAppWithMessageForWindowAsync method, RequestAccessForAppWithMessageForWindowAsync method,IProtectionPolicyManagerInterop2 interface, efswrtinterop/IProtectionPolicyManagerInterop2::RequestAccessForAppWithMessageForWindowAsync
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	efswrt.dll
api_name:
-	IProtectionPolicyManagerInterop2.RequestAccessForAppWithMessageForWindowAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Efswrt.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IProtectionPolicyManagerInterop2::RequestAccessForAppWithMessageForWindowAsync


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

An audit info object; an instance of <a href="https://msdn.microsoft.com/ibrary/windows/apps/windows.security.enterprisedata.protectionpolicyauditinfo.aspx">ProtectionPolicyAuditInfo</a>.  


### -param messageFromApp [in]

A message that will be displayed in the consent dialog so that the user can make a consent decision.  


### -param riid [iid_is] [out, retval]

  Reference to the identifier of the interface describing the type of interface pointer to return in <i>asyncOperation</i>.


### -param asyncOperation

An <a href="https://msdn.microsoft.com/library/windows/apps/br206598.aspx">IAsyncOperation<ProtectionPolicyEvaluationResult></a> with a value of the <a href="https://msdn.microsoft.com/library/windows/apps/windows.security.enterprisedata.protectionpolicyevaluationresult.aspx">ProtectionPolicyEvaluationResult</a> enumeration that is the result of the request.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B4B5BD4B-8F5F-4C1A-902E-5FB7FF75616B">IProtectionPolicyManagerInterop2</a>
 

 

