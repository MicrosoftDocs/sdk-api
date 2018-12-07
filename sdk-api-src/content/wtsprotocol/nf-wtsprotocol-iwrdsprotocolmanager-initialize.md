---
UID: NF:wtsprotocol.IWRdsProtocolManager.Initialize
title: IWRdsProtocolManager::Initialize
author: windows-sdk-content
description: Initializes the protocol manager.
old-location: termserv\iwrdsprotocolmanager_initialize.htm
tech.root: termserv
ms.assetid: c63c794c-41a0-4f07-be93-ba24dc156ca2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],Initialize method, IWRdsProtocolManager.Initialize, IWRdsProtocolManager::Initialize, Initialize, Initialize method [Remote Desktop Services], Initialize method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_initialize, wtsprotocol/IWRdsProtocolManager::Initialize
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
 - IWRdsProtocolManager.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolManager::Initialize


## -description


Initializes the protocol manager.


## -parameters




### -param pIWRdsSettings [in]

A pointer to an object that implements the <a href="https://msdn.microsoft.com/3680a001-e162-4930-985f-5c50c2e8a8b9">IWRdsProtocolSettings</a> interface.


### -param pWRdsSettings [in]

A pointer to a <a href="https://msdn.microsoft.com/38AD33F9-F955-4906-90E2-3FE5261A3E58">WRDS_SETTINGS</a> structure that contains the settings to use.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



A possible use for this method is to add a reference to the interface object pointer and to make a copy of the settings structure.




## -see-also




<a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a>
 

 

