---
UID: NF:wdstptmgmt.IWdsTransportNamespaceManager.RetrieveNamespaces
title: IWdsTransportNamespaceManager::RetrieveNamespaces method
author: windows-driver-content
description: Returns a collection of objects of the IWdsTransportNamespace interface that represent namespaces on the server that match specified criteria.
old-location: wds\iwdstransportnamespacemanager_retrievenamespaces.htm
old-project: Wds
ms.assetid: 3151ab6b-7ceb-4ecc-8480-cb5f9700ca9a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWdsTransportNamespaceManager, IWdsTransportNamespaceManager interface [Windows Deployment Services], RetrieveNamespaces method, IWdsTransportNamespaceManager::RetrieveNamespaces, RetrieveNamespaces method [Windows Deployment Services], RetrieveNamespaces method [Windows Deployment Services], IWdsTransportNamespaceManager interface, RetrieveNamespaces,IWdsTransportNamespaceManager.RetrieveNamespaces, wds.iwdstransportnamespacemanager_retrievenamespaces, wdstptmgmt/IWdsTransportNamespaceManager::RetrieveNamespaces
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
-	IWdsTransportNamespaceManager.RetrieveNamespaces
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportNamespaceManager::RetrieveNamespaces method


## -description


Returns a collection of objects of the <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a> interface that represent namespaces on the server that match specified criteria.


## -parameters




### -param bszContentProvider [in]

The name of the content provider for which namespaces are to be returned. If an empty string is specified, the method returns the namespaces for all content providers.


### -param bszNamespaceName [in]

The name of the namespace for which instances are to be returned. If an empty string is specified, the method returns all namespaces for the selected content providers. 


### -param bIncludeTombstones [in]

A value of true specifies that the method should include in the results any namespaces that have been deregistered while still having active sessions on the server. This enables an application to register another namespace with the name.  


### -param ppWdsTransportNamespaces [out]

A pointer to the object of an <a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a> interface.  This represents  a collection  of objects of an <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a> interface that match the specified criteria.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a>



<a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>



<a href="https://msdn.microsoft.com/de5fc470-af9f-4f9f-bc17-a347dc702e36">IWdsTransportNamespaceManager</a>
 

 

