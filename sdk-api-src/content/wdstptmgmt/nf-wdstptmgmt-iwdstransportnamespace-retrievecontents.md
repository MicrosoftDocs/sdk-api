---
UID: NF:wdstptmgmt.IWdsTransportNamespace.RetrieveContents
title: IWdsTransportNamespace::RetrieveContents (wdstptmgmt.h)
author: windows-sdk-content
description: Retrieves a collection of active transport content objects associated with the namespace.
old-location: wds\iwdstransportnamespace_retrievecontents.htm
tech.root: wds
ms.assetid: 78afaf1c-f29f-4ab0-8329-d2199ea49c43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWdsTransportNamespace interface [Windows Deployment Services],RetrieveContents method, IWdsTransportNamespace.RetrieveContents, IWdsTransportNamespace::RetrieveContents, RetrieveContents, RetrieveContents method [Windows Deployment Services], RetrieveContents method [Windows Deployment Services],IWdsTransportNamespace interface, wds.iwdstransportnamespace_retrievecontents, wdstptmgmt/IWdsTransportNamespace::RetrieveContents
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
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportNamespace.RetrieveContents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportNamespace::RetrieveContents


## -description


Retrieves a collection of active transport content objects associated with the namespace.


## -parameters




### -param ppWdsTransportContents [out]

A pointer to a <a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a> object that contains a collection of <a href="https://msdn.microsoft.com/d7ed1f64-578f-4b3a-b9af-9a48800b9ca4">IWdsTransportContent</a> objects that represent active sessions under this namespace.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a>



<a href="https://msdn.microsoft.com/d7ed1f64-578f-4b3a-b9af-9a48800b9ca4">IWdsTransportContent</a>



<a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>
 

 

