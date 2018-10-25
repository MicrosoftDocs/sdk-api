---
UID: NF:wtsprotocol.IWRdsProtocolManager.CreateListener
title: IWRdsProtocolManager::CreateListener
author: windows-sdk-content
description: Requests the creation of an IWRdsProtocolListener object that listens for incoming client connection requests.
old-location: termserv\iwrdsprotocolmanager_createlistener.htm
tech.root: termserv
ms.assetid: df91dc10-77af-4b5a-8033-1b1ff614bb17
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CreateListener, CreateListener method [Remote Desktop Services], CreateListener method [Remote Desktop Services],IWRdsProtocolManager interface, IWRdsProtocolManager interface [Remote Desktop Services],CreateListener method, IWRdsProtocolManager.CreateListener, IWRdsProtocolManager::CreateListener, termserv.iwrdsprotocolmanager_createlistener, wtsprotocol/IWRdsProtocolManager::CreateListener
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
 - IWRdsProtocolManager.CreateListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolManager::CreateListener


## -description


Requests the creation of an <a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a> object that listens for incoming client connection requests. The protocol provider must add a reference to the <a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a> object before returning.  The Remote Desktop Services service  releases the reference when the service stops or the listener object is deleted.


## -parameters




### -param wszListenerName [in]

A pointer to a string that contains the registry GUID that specifies the listener to create.


### -param pProtocolListener [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a> object.


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




<a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a>
 

 

