---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

