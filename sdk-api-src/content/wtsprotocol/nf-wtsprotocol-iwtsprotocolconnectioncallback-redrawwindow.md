---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.RedrawWindow
title: IWTSProtocolConnectionCallback::RedrawWindow (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnectionCallback::RedrawWindow is no longer available. Instead, use IWRdsProtocolConnectionCallback::RedrawWindow.
old-location: termserv\iwtsprotocolconnectioncallback_redrawwindow.htm
tech.root: TermServ
ms.assetid: 8c5f7167-53c0-47fd-a62d-5137c341177d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnectionCallback interface [Remote Desktop Services],RedrawWindow method, IWTSProtocolConnectionCallback.RedrawWindow, IWTSProtocolConnectionCallback::RedrawWindow, RedrawWindow, RedrawWindow method [Remote Desktop Services], RedrawWindow method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, termserv.iwtsprotocolconnectioncallback_redrawwindow, wtsprotocol/IWTSProtocolConnectionCallback::RedrawWindow
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
 - IWTSProtocolConnectionCallback.RedrawWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnectionCallback::RedrawWindow


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::RedrawWindow</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnectioncallback-redrawwindow">IWRdsProtocolConnectionCallback::RedrawWindow</a>.]

Requests that the Remote Desktop Services service redraw the client window.


## -parameters




### -param rect [in, optional]

A <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-_wts_small_rect">WTS_SMALL_RECT</a> structure that contains the x and y coordinates of the screen to redraw. A value of <b>NULL</b> requests that the entire screen be redrawn.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



This method is typically called after the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-stopscreenupdates">StopScreenUpdates</a> method.

To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside of any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-stopscreenupdates">StopScreenUpdates</a>
 

 

