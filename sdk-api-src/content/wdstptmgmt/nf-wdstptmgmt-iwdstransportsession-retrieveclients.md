---
UID: NF:wdstptmgmt.IWdsTransportSession.RetrieveClients
title: IWdsTransportSession::RetrieveClients
author: windows-sdk-content
description: Retrieves a collection of WDS clients joined to the transport session.
old-location: wds\iwdstransportsession_retrieveclients.htm
old-project: Wds
ms.assetid: c6e41658-8d91-4c15-8a5f-a9f43490890a
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWdsTransportSession interface [Windows Deployment Services],RetrieveClients method, IWdsTransportSession.RetrieveClients, IWdsTransportSession::RetrieveClients, RetrieveClients, RetrieveClients method [Windows Deployment Services], RetrieveClients method [Windows Deployment Services],IWdsTransportSession interface, wds.iwdstransportsession_retrieveclients, wdstptmgmt/IWdsTransportSession::RetrieveClients
ms.prod: windows
ms.technology: windows-sdk
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
-	IWdsTransportSession.RetrieveClients
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportSession::RetrieveClients


## -description


Retrieves a collection of WDS clients joined to the transport session.


## -parameters




### -param ppWdsTransportClients [out]

A collection of objects of the <a href="https://msdn.microsoft.com/39534411-3d69-408d-b495-10851fe40bdf">IWdsTransportClient</a> interface joined to the transport session.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/39534411-3d69-408d-b495-10851fe40bdf">IWdsTransportClient</a>



<a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a>



<a href="https://msdn.microsoft.com/acf417ea-2396-4178-84e5-6d6b495476f8">IWdsTransportSession</a>
 

 

