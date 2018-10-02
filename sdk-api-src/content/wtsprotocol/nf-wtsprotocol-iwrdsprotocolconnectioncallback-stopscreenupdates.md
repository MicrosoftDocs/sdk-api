---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.StopScreenUpdates
title: IWRdsProtocolConnectionCallback::StopScreenUpdates
author: windows-sdk-content
description: Requests that the Remote Desktop Services service stop updating the client screen.
old-location: termserv\iwrdsprotocolconnectioncallback_stopscreenupdates.htm
tech.root: TermServ
ms.assetid: 698b59d3-8391-4101-801c-8d5fd701a757
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWRdsProtocolConnectionCallback interface [Remote Desktop Services],StopScreenUpdates method, IWRdsProtocolConnectionCallback.StopScreenUpdates, IWRdsProtocolConnectionCallback::StopScreenUpdates, StopScreenUpdates, StopScreenUpdates method [Remote Desktop Services], StopScreenUpdates method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, termserv.iwrdsprotocolconnectioncallback_stopscreenupdates, wtsprotocol/IWRdsProtocolConnectionCallback::StopScreenUpdates
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnectionCallback.StopScreenUpdates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnectionCallback::StopScreenUpdates


## -description


Requests that the Remote Desktop Services service stop updating the client screen.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/81a73688-f39e-4960-8587-602d56c11e7e">IWRdsProtocolConnectionCallback</a>
 

 

