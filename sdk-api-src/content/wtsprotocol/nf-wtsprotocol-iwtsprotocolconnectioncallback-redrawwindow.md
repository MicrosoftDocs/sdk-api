---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.RedrawWindow
title: IWTSProtocolConnectionCallback::RedrawWindow
author: windows-sdk-content
description: IWTSProtocolConnectionCallback::RedrawWindow is no longer available. Instead, use IWRdsProtocolConnectionCallback::RedrawWindow.
old-location: termserv\iwtsprotocolconnectioncallback_redrawwindow.htm
tech.root: termserv
ms.assetid: 8c5f7167-53c0-47fd-a62d-5137c341177d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWTSProtocolConnectionCallback interface [Remote Desktop Services],RedrawWindow method, IWTSProtocolConnectionCallback.RedrawWindow, IWTSProtocolConnectionCallback::RedrawWindow, RedrawWindow, RedrawWindow method [Remote Desktop Services], RedrawWindow method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, termserv.iwtsprotocolconnectioncallback_redrawwindow, wtsprotocol/IWTSProtocolConnectionCallback::RedrawWindow
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
 - IWTSProtocolConnectionCallback.RedrawWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolConnectionCallback::RedrawWindow


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::RedrawWindow</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/92d52015-c5b9-472e-898b-aca6f6e83620">IWRdsProtocolConnectionCallback::RedrawWindow</a>.]

Requests that the Remote Desktop Services service redraw the client window.


## -parameters




### -param rect [in, optional]

A <a href="https://msdn.microsoft.com/5f139077-8ef4-4c8e-ae33-0dd3aee58ef6">WTS_SMALL_RECT</a> structure that contains the x and y coordinates of the screen to redraw. A value of <b>NULL</b> requests that the entire screen be redrawn.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method is typically called after the <a href="https://msdn.microsoft.com/69fab470-8763-405e-96f1-d3b1c5a26422">StopScreenUpdates</a> method.

To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside of any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a>



<a href="https://msdn.microsoft.com/69fab470-8763-405e-96f1-d3b1c5a26422">StopScreenUpdates</a>
 

 

