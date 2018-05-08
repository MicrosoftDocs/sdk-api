---
UID: NF:wdstptmgmt.IWdsTransportManager.GetWdsTransportServer
title: IWdsTransportManager::GetWdsTransportServer
author: windows-driver-content
description: Creates an object of the IWdsTransportServer interface that can be used to manage a WDS transport server. The method confirms that the system can reach a WDS transport server with the specified name.
old-location: wds\iwdstransportmanager_getwdstransportserver.htm
old-project: Wds
ms.assetid: 537f75d1-43aa-4f18-a39b-ad45148c1246
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetWdsTransportServer, GetWdsTransportServer method [Windows Deployment Services], GetWdsTransportServer method [Windows Deployment Services],IWdsTransportManager interface, IWdsTransportManager interface [Windows Deployment Services],GetWdsTransportServer method, IWdsTransportManager.GetWdsTransportServer, IWdsTransportManager::GetWdsTransportServer, wds.iwdstransportmanager_getwdstransportserver, wdstptmgmt/IWdsTransportManager::GetWdsTransportServer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wdstptmgmt.dll
api_name:
-	IWdsTransportManager.GetWdsTransportServer
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportManager::GetWdsTransportServer


## -description


Creates an object of the <a href="https://msdn.microsoft.com/0129658d-8725-4020-ae9c-9d0a44075561">IWdsTransportServer</a> interface that can be used to manage a WDS transport server. The method confirms that the system can reach a WDS transport server with the specified name.


## -parameters




### -param bszServerName [in]

The name of the WDS transport server to be represented by this object. This can be a NetBIOS name or a fully qualified DNS name. If the value is an empty string, the object represents the local computer.


### -param ppWdsTransportServer [out]

A pointer to the object of the  <a href="https://msdn.microsoft.com/0129658d-8725-4020-ae9c-9d0a44075561">IWdsTransportServer</a> interface. 


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/23f36ec7-5f6f-486c-bb09-e2f5b6f57efa">IWdsTransportManager</a>



<a href="https://msdn.microsoft.com/0129658d-8725-4020-ae9c-9d0a44075561">IWdsTransportServer</a>
 

 

