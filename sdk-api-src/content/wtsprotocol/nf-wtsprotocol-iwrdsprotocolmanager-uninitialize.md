---
UID: NF:wtsprotocol.IWRdsProtocolManager.Uninitialize
title: IWRdsProtocolManager::Uninitialize (wtsprotocol.h)
description: Uninitializes the protocol manager.
helpviewer_keywords: ["IWRdsProtocolManager interface [Remote Desktop Services]","Uninitialize method","IWRdsProtocolManager.Uninitialize","IWRdsProtocolManager::Uninitialize","Uninitialize","Uninitialize method [Remote Desktop Services]","Uninitialize method [Remote Desktop Services]","IWRdsProtocolManager interface","termserv.iwrdsprotocolmanager_uninitialize","wtsprotocol/IWRdsProtocolManager::Uninitialize"]
old-location: termserv\iwrdsprotocolmanager_uninitialize.htm
tech.root: TermServ
ms.assetid: 1d7bc6e3-798e-4dc8-8892-7be6992b67ab
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],Uninitialize method, IWRdsProtocolManager.Uninitialize, IWRdsProtocolManager::Uninitialize, Uninitialize, Uninitialize method [Remote Desktop Services], Uninitialize method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_uninitialize, wtsprotocol/IWRdsProtocolManager::Uninitialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsProtocolManager::Uninitialize
 - wtsprotocol/IWRdsProtocolManager::Uninitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolManager.Uninitialize
---

# IWRdsProtocolManager::Uninitialize


## -description

Uninitializes the protocol manager.



## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You can implement this method to clean up resources used by the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize">Initialize</a> method. For example, if the <b>Initialize</b> method added a reference to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings">IWRdsProtocolSettings</a> object pointer, the <b>Uninitialize</b> method can release that reference.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a>



<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize">Initialize</a>
