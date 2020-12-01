---
UID: NF:eaphostpeerconfigapis.EapHostPeerFreeErrorMemory
title: EapHostPeerFreeErrorMemory function (eaphostpeerconfigapis.h)
description: Frees memory allocated to an EAP_ERROR structure.
helpviewer_keywords: ["EapHostPeerFreeErrorMemory","EapHostPeerFreeErrorMemory function [EAPHost]","eaphost.eaphostpeerfreeerrormemory","eaphostpeerconfigapis/EapHostPeerFreeErrorMemory"]
old-location: eaphost\eaphostpeerfreeerrormemory.htm
tech.root: eaphost
ms.assetid: c80ac625-8202-49a7-813a-62a9e0d15058
ms.date: 12/05/2018
ms.keywords: EapHostPeerFreeErrorMemory, EapHostPeerFreeErrorMemory function [EAPHost], eaphost.eaphostpeerfreeerrormemory, eaphostpeerconfigapis/EapHostPeerFreeErrorMemory
req.header: eaphostpeerconfigapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerFreeErrorMemory
 - eaphostpeerconfigapis/EapHostPeerFreeErrorMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerFreeErrorMemory
---

# EapHostPeerFreeErrorMemory function


## -description

Frees memory allocated to an [EAPHost supplicant configuration function](/windows/win32/eaphost/eap-host-supplicant-configuration-functions) fails. 

The  <b>EapHostPeerFreeErrorMemory</b> function is used only for freeing <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structures returned by EAPHost configuration APIs, while the <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a> function is used for freeing <b>EAP_ERROR</b> structures returned by EAPHost run-time APIs.

If any  of the following configuration APIs functions are called, and an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> is returned, <b>EapHostPeerFreeErrorMemory</b> must be called to free the memory:<ul>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigblob2xml">EapHostPeerConfigBlob2Xml</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob">EapHostPeerConfigXml2Blob</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob">EapHostPeerCredentialsXml2Blob</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui">EapHostPeerInvokeConfigUI</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields">EapHostPeerQueryCredentialsInputFields</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields">EapHostPeerQueryUserBlobFromCredentialsInputFields</a>
</li>
</ul>

<div class="alert"><b>Note</b>  EAPHost run-time APIs are defined in eappapis.h. EAPHost configuration APIs are defined in  EapHostPeerConfigApis.h. </div><div> </div>

## -parameters

### -param pEapError

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that  contains the error data to free.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[EAPHost Supplicant Frequently Asked Questions](/windows/win32/eaphost/eaphost-supplicant-frequently-asked-questions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostFreeEapError</a>