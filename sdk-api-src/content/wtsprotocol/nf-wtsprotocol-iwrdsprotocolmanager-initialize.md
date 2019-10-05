---
UID: NF:wtsprotocol.IWRdsProtocolManager.Initialize
title: IWRdsProtocolManager::Initialize (wtsprotocol.h)
author: windows-sdk-content
description: Initializes the protocol manager.
old-location: termserv\iwrdsprotocolmanager_initialize.htm
tech.root: TermServ
ms.assetid: c63c794c-41a0-4f07-be93-ba24dc156ca2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],Initialize method, IWRdsProtocolManager.Initialize, IWRdsProtocolManager::Initialize, Initialize, Initialize method [Remote Desktop Services], Initialize method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_initialize, wtsprotocol/IWRdsProtocolManager::Initialize
ms.topic: method
f1_keywords:
- wtsprotocol/IWRdsProtocolManager.Initialize
dev_langs:
 - c++
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
- IWRdsProtocolManager.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolManager::Initialize


## -description


Initializes the protocol manager.


## -parameters




### -param pIWRdsSettings [in]

A pointer to an object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings">IWRdsProtocolSettings</a> interface.


### -param pWRdsSettings [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings">WRDS_SETTINGS</a> structure that contains the settings to use.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



A possible use for this method is to add a reference to the interface object pointer and to make a copy of the settings structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a>
 

 

