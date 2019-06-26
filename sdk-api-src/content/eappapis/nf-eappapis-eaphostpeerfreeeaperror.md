---
UID: NF:eappapis.EapHostPeerFreeEapError
title: EapHostPeerFreeEapError function (eappapis.h)
author: windows-sdk-content
description: Frees EAP_ERROR structures returned by EAPHost run-time APIs.
old-location: eaphost\eaphostpeerfreeeaperror.htm
tech.root: eaphost
ms.assetid: 36f9b5dd-821d-4cc5-a1dd-587098635d17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerFreeEapError, EapHostPeerFreeEapError function [EAPHost], eaphost.eaphostpeerfreeeaperror, eappapis/EapHostPeerFreeEapError
ms.topic: function
f1_keywords: 
 - "eappapis/EapHostPeerFreeEapError"
req.header: eappapis.h
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerFreeEapError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapHostPeerFreeEapError function


## -description


Frees <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structures returned by EAPHost run-time APIs. 

In contrast, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a> function is used only for freeing <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structures returned by EAPHost configuration APIs. 

If any  of the following run-time APIs are called and an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> is returned, <b>EapHostPeerFreeEapError</b> must be called to free the memory:<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection">EapHostPeerClearConnection</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus">EapHostPeerGetAuthStatus</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes">EapHostPeerGetResponseAttributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult">EapHostPeerGetResult</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket">EapHostPeerGetSendPacket</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext">EapHostPeerGetUIContext</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket">EapHostPeerProcessReceivedPacket</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes">EapHostPeerSetResponseAttributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext">EapHostPeerSetUIContext</a>
</li>
</ul>

<div class="alert"><b>Note</b>  EAPHost run-time APIs are defined in eappapis.h. EAPHost configuration APIs are defined in  EapHostPeerConfigApis.h.</div><div> </div>

## -parameters




### -param pEapError [in]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure that  contains the error data to free.


## -returns



This function does not return a value.




## -remarks



To release all memory allocated by EAPHost for a authentication session, the caller must call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>. To release all memory allocated by EAPHost for a connection, the caller must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection">EapHostPeerClearConnection</a> function.

<b>EapHostPeerFreeEapError</b> is not thread safe. Any given <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> must be freed on one thread only. Do not call  <b>EapHostPeerFreeEapError</b> twice on the same <b>EAP_ERROR</b> structure. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-configuration-functions">EAPHost Supplicant Configuration Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphost-supplicant-frequently-asked-questions">EAPHost Supplicant Frequently Asked Questions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>
 

 

