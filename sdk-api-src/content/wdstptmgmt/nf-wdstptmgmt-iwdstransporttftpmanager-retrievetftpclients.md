---
UID: NF:wdstptmgmt.IWdsTransportTftpManager.RetrieveTftpClients
title: IWdsTransportTftpManager::RetrieveTftpClients (wdstptmgmt.h)
author: windows-sdk-content
description: Returns a pointer to the object of an IWdsTransportCollection interface containing a collection of objects of the IWdsTransportTftpClient interface for the clients currently connected to the TFTP server.
old-location: wds\iwdstransporttftpclient_retrievetftpclients.htm
tech.root: wds
ms.assetid: 48527950-A29D-4BC0-AD85-7B40E9C19133
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWdsTransportTftpManager interface [Windows Deployment Services],RetrieveTftpClients method, IWdsTransportTftpManager.RetrieveTftpClients, IWdsTransportTftpManager::RetrieveTftpClients, RetrieveTftpClients, RetrieveTftpClients method [Windows Deployment Services], RetrieveTftpClients method [Windows Deployment Services],IWdsTransportTftpManager interface, wds.iwdstransporttftpclient_retrievetftpclients, wdstptmgmt/IWdsTransportTftpManager::RetrieveTftpClients
ms.topic: method
f1_keywords: ["wdstptmgmt/IWdsTransportTftpManager.RetrieveTftpClients"]
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IWdsTransportTftpManager.RetrieveTftpClients
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportTftpManager::RetrieveTftpClients


## -description


Returns a pointer to the object of an <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a> interface containing a collection of objects of the <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransporttftpclient">IWdsTransportTftpClient</a> interface for the clients currently connected to the TFTP server. 


## -parameters




### -param ppWdsTransportTftpClients [out, retval]

A pointer to a pointer to an object of the <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a> interface. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransporttftpmanager">IWdsTransportTftpManager</a>
 

 

