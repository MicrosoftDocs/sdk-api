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

# EapHostPeerFreeEapError function


## -description


Frees <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structures returned by EAPHost run-time APIs. 

In contrast, the <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a> function is used only for freeing <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structures returned by EAPHost configuration APIs. 

If any  of the following run-time APIs are called and an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> is returned, <b>EapHostPeerFreeEapError</b> must be called to free the memory:<ul>
<li>
<a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d997e4e-6e7f-47db-9957-9658e54c0bdf">EapHostPeerClearConnection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cb5ceffb-941f-48ad-9271-111f41adc65b">EapHostPeerGetAuthStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/84df4877-9ac9-4ab5-a357-276880051ff0">EapHostPeerGetResponseAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1f0fc05-d9cd-4a37-ba74-89ac9948a292">EapHostPeerGetResult</a>
</li>
<li>
<a href="https://msdn.microsoft.com/22e17496-e381-415e-8da0-88aad37d0d21">EapHostPeerGetSendPacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/47ade6f1-067b-48ab-b4ac-a3d3cf63d809">EapHostPeerGetUIContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b3bc23d-312d-494d-afd0-ce82d2d5136c">EapHostPeerProcessReceivedPacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8ce5510-f5ba-403c-8709-940ae58cd10d">EapHostPeerSetResponseAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f532dd65-d807-4880-9339-ba233e0faa38">EapHostPeerSetUIContext</a>
</li>
</ul>

<div class="alert"><b>Note</b>  EAPHost run-time APIs are defined in eappapis.h. EAPHost configuration APIs are defined in  EapHostPeerConfigApis.h.</div><div> </div>

## -parameters




### -param pEapError

TBD




#### - ppEapError [in]

A pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that  contains the error data to free.


## -returns



This function does not return a value.




## -remarks



To release all memory allocated by EAPHost for a authentication session, the caller must call <a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>. To release all memory allocated by EAPHost for a connection, the caller must call the <a href="https://msdn.microsoft.com/1d997e4e-6e7f-47db-9957-9658e54c0bdf">EapHostPeerClearConnection</a> function.

<b>EapHostPeerFreeEapError</b> is not thread safe. Any given <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> must be freed on one thread only. Do not call  <b>EapHostPeerFreeEapError</b> twice on the same <b>EAP_ERROR</b> structure. 




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/bf8db711-386e-47c2-be47-4cfd6c4d8d9e">EAPHost Supplicant Frequently Asked Questions</a>



<a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>
 

 

