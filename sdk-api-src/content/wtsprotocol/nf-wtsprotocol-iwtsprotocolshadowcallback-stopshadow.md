---
UID: NF:wtsprotocol.IWTSProtocolShadowCallback.StopShadow
title: IWTSProtocolShadowCallback::StopShadow
author: windows-sdk-content
description: IWTSProtocolShadowCallback::StopShadow is no longer available. Instead, use IWRdsProtocolShadowCallback::StopShadow.
old-location: termserv\iwtsprotocolshadowcallback_stopshadow.htm
tech.root: TermServ
ms.assetid: 54e47922-aea5-4e2f-b329-94300fc1ac3d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWTSProtocolShadowCallback interface [Remote Desktop Services],StopShadow method, IWTSProtocolShadowCallback.StopShadow, IWTSProtocolShadowCallback::StopShadow, StopShadow, StopShadow method [Remote Desktop Services], StopShadow method [Remote Desktop Services],IWTSProtocolShadowCallback interface, termserv.iwtsprotocolshadowcallback_stopshadow, wtsprotocol/IWTSProtocolShadowCallback::StopShadow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IWTSProtocolShadowCallback::StopShadow


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowCallback::StopShadow</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/09911813-554d-4ce1-b34e-5a6f57ec286d">IWRdsProtocolShadowCallback::StopShadow</a>.]

Instructs the Remote Desktop Services service to stop shadowing a target. This method is called in response to a call of <a href="https://msdn.microsoft.com/437983a4-48a4-4b37-99ba-35fe1f03b3ec">DoTarget</a> by the shadow client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/ce224b9f-161c-4133-97d9-05c339eefb77">IWTSProtocolShadowCallback</a>
 

 

