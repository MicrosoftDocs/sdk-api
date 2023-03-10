---
UID: NF:wtsprotocol.IWTSProtocolManager.CreateListener
title: IWTSProtocolManager::CreateListener (wtsprotocol.h)
description: IWTSProtocolManager::CreateListener is no longer available. Instead, use IWRdsProtocolManager::CreateListener.
helpviewer_keywords: ["CreateListener","CreateListener method [Remote Desktop Services]","CreateListener method [Remote Desktop Services]","IWTSProtocolManager interface","IWTSProtocolManager interface [Remote Desktop Services]","CreateListener method","IWTSProtocolManager.CreateListener","IWTSProtocolManager::CreateListener","termserv.iwtsprotocolmanager_createlistener","wtsprotocol/IWTSProtocolManager::CreateListener"]
old-location: termserv\iwtsprotocolmanager_createlistener.htm
tech.root: TermServ
ms.assetid: 2c947181-5cac-40c1-b993-537b580efafe
ms.date: 12/05/2018
ms.keywords: CreateListener, CreateListener method [Remote Desktop Services], CreateListener method [Remote Desktop Services],IWTSProtocolManager interface, IWTSProtocolManager interface [Remote Desktop Services],CreateListener method, IWTSProtocolManager.CreateListener, IWTSProtocolManager::CreateListener, termserv.iwtsprotocolmanager_createlistener, wtsprotocol/IWTSProtocolManager::CreateListener
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolManager::CreateListener
 - wtsprotocol/IWTSProtocolManager::CreateListener
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolManager.CreateListener
---

# IWTSProtocolManager::CreateListener


## -description

<p class="CCE_Message">[<b>IWTSProtocolManager::CreateListener</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener">IWRdsProtocolManager::CreateListener</a>.]

Requests the creation of an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a> object that listens for incoming client connection requests. The protocol provider must add a reference to the <b>IWTSProtocolListener</b> object before returning.  The Remote Desktop Services service  releases the reference when the service stops or the listener object is deleted.

## -parameters

### -param wszListenerName [in]

A pointer to a string that contains the registry GUID that specifies the listener to create.

### -param pProtocolListener [out]

The address of a pointer to the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a> object.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>CreateListener</b> method is the first call the Remote Desktop Services service  makes into your  protocol provider. The service looks in the registry under the following key to find the GUID of the listener to create:


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>System</b>
      <b>CurrentControlSet</b>
         <b>Control</b>
            <b>Terminal Server</b>
               <b>WinStations</b>
                  <b><i>ListenerName</i></b>
                     <b>LoadableProtocol_Object</b></pre>

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager">IWTSProtocolManager</a>
