---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.RedrawWindow
title: IWRdsProtocolConnectionCallback::RedrawWindow
author: windows-sdk-content
description: Requests that the Remote Desktop Services service redraw the client window.
old-location: termserv\iwrdsprotocolconnectioncallback_redrawwindow.htm
old-project: termserv
ms.assetid: 92d52015-c5b9-472e-898b-aca6f6e83620
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IWRdsProtocolConnectionCallback interface [Remote Desktop Services],RedrawWindow method, IWRdsProtocolConnectionCallback.RedrawWindow, IWRdsProtocolConnectionCallback::RedrawWindow, RedrawWindow, RedrawWindow method [Remote Desktop Services], RedrawWindow method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, termserv.iwrdsprotocolconnectioncallback_redrawwindow, wtsprotocol/IWRdsProtocolConnectionCallback::RedrawWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnectionCallback.RedrawWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnectionCallback::RedrawWindow


## -description


Requests that the Remote Desktop Services service redraw the client window.


## -parameters




### -param rect [in, optional]

A <a href="https://msdn.microsoft.com/5f139077-8ef4-4c8e-ae33-0dd3aee58ef6">WRDS_SMALL_RECT</a> structure that contains the x and y coordinates of the screen to redraw. A value of <b>NULL</b> requests that the entire screen be redrawn.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method is typically called after the <a href="https://msdn.microsoft.com/698b59d3-8391-4101-801c-8d5fd701a757">StopScreenUpdates</a> method.

To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/81a73688-f39e-4960-8587-602d56c11e7e">IWRdsProtocolConnectionCallback</a>
 

 

