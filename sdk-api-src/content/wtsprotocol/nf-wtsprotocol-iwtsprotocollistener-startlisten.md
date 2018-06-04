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

# IWTSProtocolListener::StartListen


## -description


<p class="CCE_Message">[<b>IWTSProtocolListener::StartListen</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/d3797411-2ac6-4d3c-8c90-5c566e6d8fa8">IWRdsProtocolListener::StartListen</a>.]

 Notifies the protocol to start listening for client connection requests.


## -parameters




### -param pCallback [in]

A pointer to an <a href="https://msdn.microsoft.com/607fcb85-4602-4651-b246-3e32c8868e47">IWTSProtocolListenerCallback</a> object 
implemented by the Remote Desktop Services
 service. The protocol uses the 
<b>IWTSProtocolListenerCallback</b> object to notify 
the 

Remote Desktop Services 
service about incoming connection requests. The protocol must add a reference to this object and release it when 
<a href="https://msdn.microsoft.com/5c5b09d3-74d6-4067-b18b-ed2a54af4153">StopListen</a> is called.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, 
return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, 
see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>StartListen</b> method is called when the Remote Desktop Services service starts.

<ol>
<li>The Remote Desktop Services service calls <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create an  <a href="https://msdn.microsoft.com/a54bdb46-b18b-4a6d-90fc-75947f6dd191">IWTSProtocolManager</a> object.</li>
<li>The Remote Desktop Services service calls <a href="https://msdn.microsoft.com/2c947181-5cac-40c1-b993-537b580efafe">CreateListener</a> on the <a href="https://msdn.microsoft.com/a54bdb46-b18b-4a6d-90fc-75947f6dd191">IWTSProtocolManager</a> interface. The protocol creates an <a href="https://msdn.microsoft.com/b11eb19f-ffc3-4a68-85c6-90a2412168f8">IWTSProtocolListener</a> object and passes it back to the Remote Desktop Services service.</li>
<li>The Remote Desktop Services service calls <b>StartListen</b> on the <a href="https://msdn.microsoft.com/b11eb19f-ffc3-4a68-85c6-90a2412168f8">IWTSProtocolListener</a> object.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/b11eb19f-ffc3-4a68-85c6-90a2412168f8">IWTSProtocolListener</a>
 

 

