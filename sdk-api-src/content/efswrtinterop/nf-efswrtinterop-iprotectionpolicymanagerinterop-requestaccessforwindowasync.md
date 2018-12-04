---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop.RequestAccessForWindowAsync
title: IProtectionPolicyManagerInterop::RequestAccessForWindowAsync
author: windows-sdk-content
description: Request access to enterprise protected content for an identity.
old-location: edp\iprotectionpolicymanager_requestaccessforwindowasync.htm
tech.root: EDP
ms.assetid: F32A24C6-0913-4EB9-8462-6AA734429D7E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EDP.iprotectionpolicymanager_requestaccessforwindowasync, IProtectionPolicyManagerInterop interface,RequestAccessForWindowAsync method, IProtectionPolicyManagerInterop.RequestAccessForWindowAsync, IProtectionPolicyManagerInterop::RequestAccessForWindowAsync, RequestAccessForWindowAsync, RequestAccessForWindowAsync method, RequestAccessForWindowAsync method,IProtectionPolicyManagerInterop interface, efswrtinterop/IProtectionPolicyManagerInterop::RequestAccessForWindowAsync
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
 - IProtectionPolicyManagerInterop.RequestAccessForWindowAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProtectionPolicyManagerInterop::RequestAccessForWindowAsync


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Request access to enterprise protected content for an identity.


## -parameters




### -param appWindow [in]

A handle to the current window.


### -param sourceIdentity [in]

The enterprise identity to which the content is protected. This is an email address or domain that is managed. 


### -param targetIdentity [in]

 The enterprise identity to which the content is being disclosed. This is an email address or domain.


### -param riid [iid_is] [out, retval]

Reference to the identifier of the interface describing the type of interface pointer to return in <i>asyncOperation</i>.


### -param asyncOperation

An <a href="https://msdn.microsoft.com/library/windows/apps/br206598.aspx">IAsyncOperation<ProtectionPolicyEvaluationResult></a> with a value of the <a href="https://msdn.microsoft.com/library/windows/apps/windows.security.enterprisedata.protectionpolicyevaluationresult.aspx">ProtectionPolicyEvaluationResult</a> enumeration that is the result of the request.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/AFA7F918-8730-40A2-871E-9356391B47F8">IProtectionPolicyManagerInterop</a>
 

 

