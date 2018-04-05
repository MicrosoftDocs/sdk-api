---
UID: NF:wdstptmgmt.IWdsTransportNamespaceManager.RetrieveNamespace
title: IWdsTransportNamespaceManager::RetrieveNamespace method
author: windows-driver-content
description: Retrieves, by name, an object of an IWdsTransportNamespace interface. The name should be registered with the namespace on the WDS transport server.
old-location: wds\iwdstransportnamespacemanager_retrievenamespace.htm
old-project: Wds
ms.assetid: 8afe8d0c-4c6b-45a6-a330-b2cee59ca1ad
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWdsTransportNamespaceManager, IWdsTransportNamespaceManager interface [Windows Deployment Services], RetrieveNamespace method, IWdsTransportNamespaceManager::RetrieveNamespace, RetrieveNamespace method [Windows Deployment Services], RetrieveNamespace method [Windows Deployment Services], IWdsTransportNamespaceManager interface, RetrieveNamespace,IWdsTransportNamespaceManager.RetrieveNamespace, wds.iwdstransportnamespacemanager_retrievenamespace, wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespace
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
-	IWdsTransportNamespaceManager.RetrieveNamespace
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportNamespaceManager::RetrieveNamespace method


## -description


Retrieves,  by name, an object of an <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a> interface. The name  should be registered with the namespace on the WDS transport server.


## -parameters




### -param bszNamespaceName [in]

The name of the namespace for which an object is being returned.  The namespace should be registered with the WDS transport server. 


### -param ppWdsTransportNamespace [out]

A pointer to the object of an <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a> interface that matches the specified name.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>



<a href="https://msdn.microsoft.com/de5fc470-af9f-4f9f-bc17-a347dc702e36">IWdsTransportNamespaceManager</a>
 

 

