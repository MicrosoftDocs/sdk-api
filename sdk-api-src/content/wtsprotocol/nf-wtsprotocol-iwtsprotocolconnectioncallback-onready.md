---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWTSProtocolConnectionCallback::OnReady


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::OnReady</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/88134a34-c494-48ea-9063-206e7d0c5139">IWRdsProtocolConnectionCallback::OnReady</a>.]

Requests that the Remote Desktop Services service continue the connection process for that client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The protocol must call this method after the Remote Desktop Services service calls <a href="https://msdn.microsoft.com/b3fcc213-8257-433f-b304-ce19bc209591">SendPolicyData</a>. The Remote Desktop Services service will not call <a href="https://msdn.microsoft.com/5be00911-f68a-410d-8d56-81458b5ff44e">AcceptConnection</a> to continue the connection process until <b>OnReady</b> has been called.




## -see-also




<a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a>
 

 

