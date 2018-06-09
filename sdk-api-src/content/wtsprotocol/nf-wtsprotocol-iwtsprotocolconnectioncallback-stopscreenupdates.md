---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.StopScreenUpdates
title: IWTSProtocolConnectionCallback::StopScreenUpdates
author: windows-sdk-content
description: IWTSProtocolConnectionCallback::StopScreenUpdates is no longer available. Instead, use IWRdsProtocolConnectionCallback::StopScreenUpdates.
old-location: termserv\iwtsprotocolconnectioncallback_stopscreenupdates.htm
old-project: TermServ
ms.assetid: 69fab470-8763-405e-96f1-d3b1c5a26422
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWTSProtocolConnectionCallback interface [Remote Desktop Services],StopScreenUpdates method, IWTSProtocolConnectionCallback.StopScreenUpdates, IWTSProtocolConnectionCallback::StopScreenUpdates, StopScreenUpdates, StopScreenUpdates method [Remote Desktop Services], StopScreenUpdates method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, termserv.iwtsprotocolconnectioncallback_stopscreenupdates, wtsprotocol/IWTSProtocolConnectionCallback::StopScreenUpdates
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnectionCallback.StopScreenUpdates
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnectionCallback::StopScreenUpdates


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::StopScreenUpdates</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/698b59d3-8391-4101-801c-8d5fd701a757">IWRdsProtocolConnectionCallback::StopScreenUpdates</a>.]

Requests that the Remote Desktop Services service stop updating the client screen.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside of any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a>
 

 

