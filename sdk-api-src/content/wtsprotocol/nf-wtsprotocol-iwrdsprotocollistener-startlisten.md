---
UID: NF:wtsprotocol.IWRdsProtocolListener.StartListen
title: IWRdsProtocolListener::StartListen
author: windows-driver-content
description: Notifies the protocol to start listening for client connection requests.
old-location: termserv\iwrdsprotocollistener_startlisten.htm
old-project: TermServ
ms.assetid: d3797411-2ac6-4d3c-8c90-5c566e6d8fa8
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IWRdsProtocolListener interface [Remote Desktop Services],StartListen method, IWRdsProtocolListener.StartListen, IWRdsProtocolListener::StartListen, StartListen, StartListen method [Remote Desktop Services], StartListen method [Remote Desktop Services],IWRdsProtocolListener interface, termserv.iwrdsprotocollistener_startlisten, wtsprotocol/IWRdsProtocolListener::StartListen
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWRdsProtocolListener.StartListen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolListener::StartListen


## -description


Notifies the protocol to start listening for client connection requests.


## -parameters




### -param pCallback [in]

A pointer to an <a href="https://msdn.microsoft.com/33f583a4-8311-4db1-9646-bed1cd06e479">IWRdsProtocolListenerCallback</a> object 
implemented by the Remote Desktop Services
 service. The protocol uses the 
<b>IWRdsProtocolListenerCallback</b> object to notify 
the 

Remote Desktop Services 
service about incoming connection requests. The protocol must add a reference to this object and release it when 
<a href="https://msdn.microsoft.com/bfb758e8-3d71-47b9-bf7d-075c0c401177">StopListen</a> is called.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, 
return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, 
see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>StartListen</b> method is called when the Remote Desktop Services service starts.

<ol>
<li>The Remote Desktop Services service calls <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create an  <a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a> object.</li>
<li>The Remote Desktop Services service calls <a href="https://msdn.microsoft.com/df91dc10-77af-4b5a-8033-1b1ff614bb17">CreateListener</a> on the <a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a> interface. The protocol creates an <a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a> object and passes it back to the Remote Desktop Services service.</li>
<li>The Remote Desktop Services service calls <b>StartListen</b> on the <a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a> object.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a>
 

 

