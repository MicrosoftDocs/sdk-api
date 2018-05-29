---
UID: NF:wtsprotocol.IWRdsProtocolManager.Uninitialize
title: IWRdsProtocolManager::Uninitialize
author: windows-sdk-content
description: Uninitializes the protocol manager.
old-location: termserv\iwrdsprotocolmanager_uninitialize.htm
old-project: TermServ
ms.assetid: 1d7bc6e3-798e-4dc8-8892-7be6992b67ab
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],Uninitialize method, IWRdsProtocolManager.Uninitialize, IWRdsProtocolManager::Uninitialize, Uninitialize, Uninitialize method [Remote Desktop Services], Uninitialize method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_uninitialize, wtsprotocol/IWRdsProtocolManager::Uninitialize
ms.prod: windows
ms.technology: windows-sdk
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
-	IWRdsProtocolManager.Uninitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolManager::Uninitialize


## -description


Uninitializes the protocol manager.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You can implement this method to clean up resources used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method. For example, if the <b>Initialize</b> method added a reference to an <a href="https://msdn.microsoft.com/3680a001-e162-4930-985f-5c50c2e8a8b9">IWRdsProtocolSettings</a> object pointer, the <b>Uninitialize</b> method can release that reference.




## -see-also




<a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
 

 

