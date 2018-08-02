---
UID: NF:wtsprotocol.IWTSProtocolManager.CreateListener
title: IWTSProtocolManager::CreateListener
author: windows-sdk-content
description: IWTSProtocolManager::CreateListener is no longer available. Instead, use IWRdsProtocolManager::CreateListener.
old-location: termserv\iwtsprotocolmanager_createlistener.htm
old-project: TermServ
ms.assetid: 2c947181-5cac-40c1-b993-537b580efafe
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateListener, CreateListener method [Remote Desktop Services], CreateListener method [Remote Desktop Services],IWTSProtocolManager interface, IWTSProtocolManager interface [Remote Desktop Services],CreateListener method, IWTSProtocolManager.CreateListener, IWTSProtocolManager::CreateListener, termserv.iwtsprotocolmanager_createlistener, wtsprotocol/IWTSProtocolManager::CreateListener
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolManager.CreateListener
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

