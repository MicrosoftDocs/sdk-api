---
UID: NF:wtsprotocol.IWTSProtocolShadowCallback.StopShadow
title: IWTSProtocolShadowCallback::StopShadow (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolShadowCallback::StopShadow is no longer available. Instead, use IWRdsProtocolShadowCallback::StopShadow.
old-location: termserv\iwtsprotocolshadowcallback_stopshadow.htm
tech.root: TermServ
ms.assetid: 54e47922-aea5-4e2f-b329-94300fc1ac3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSProtocolShadowCallback interface [Remote Desktop Services],StopShadow method, IWTSProtocolShadowCallback.StopShadow, IWTSProtocolShadowCallback::StopShadow, StopShadow, StopShadow method [Remote Desktop Services], StopShadow method [Remote Desktop Services],IWTSProtocolShadowCallback interface, termserv.iwtsprotocolshadowcallback_stopshadow, wtsprotocol/IWTSProtocolShadowCallback::StopShadow
ms.topic: method
f1_keywords: 
 - "wtsprotocol/IWTSProtocolShadowCallback.StopShadow"
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolShadowCallback.StopShadow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolShadowCallback::StopShadow


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowCallback::StopShadow</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolshadowcallback-stopshadow">IWRdsProtocolShadowCallback::StopShadow</a>.]

Instructs the Remote Desktop Services service to stop shadowing a target. This method is called in response to a call of <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolshadowconnection-dotarget">DoTarget</a> by the shadow client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback">IWTSProtocolShadowCallback</a>
 

 

