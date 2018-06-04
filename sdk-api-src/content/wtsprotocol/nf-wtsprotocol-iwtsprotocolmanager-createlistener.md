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

# IWTSProtocolManager::CreateListener


## -description


<p class="CCE_Message">[<b>IWTSProtocolManager::CreateListener</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/df91dc10-77af-4b5a-8033-1b1ff614bb17">IWRdsProtocolManager::CreateListener</a>.]

Requests the creation of an <a href="https://msdn.microsoft.com/b11eb19f-ffc3-4a68-85c6-90a2412168f8">IWTSProtocolListener</a> object that listens for incoming client connection requests. The protocol provider must add a reference to the <b>IWTSProtocolListener</b> object before returning.  The Remote Desktop Services service  releases the reference when the service stops or the listener object is deleted.


## -parameters




### -param wszListenerName [in]

A pointer to a string that contains the registry GUID that specifies the listener to create.


### -param pProtocolListener [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/b11eb19f-ffc3-4a68-85c6-90a2412168f8">IWTSProtocolListener</a> object.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -remarks



The <b>CreateListener</b> method is the first call the Remote Desktop Services service  makes into your  protocol provider. The service looks in the registry under the following key to find the GUID of the listener to create:


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>System</b>
      <b>CurrentControlSet</b>
         <b>Control</b>
            <b>Terminal Server</b>
               <b>WinStations</b>
                  <b><i>ListenerName</i></b>
                     <b>LoadableProtocol_Object</b></pre>





## -see-also




<a href="https://msdn.microsoft.com/a54bdb46-b18b-4a6d-90fc-75947f6dd191">IWTSProtocolManager</a>
 

 

