---
UID: NF:wdstptmgmt.IWdsTransportTftpManager.RetrieveTftpClients
title: IWdsTransportTftpManager::RetrieveTftpClients (wdstptmgmt.h)
description: Returns a pointer to the object of an IWdsTransportCollection interface containing a collection of objects of the IWdsTransportTftpClient interface for the clients currently connected to the TFTP server.
helpviewer_keywords: ["IWdsTransportTftpManager interface [Windows Deployment Services]","RetrieveTftpClients method","IWdsTransportTftpManager.RetrieveTftpClients","IWdsTransportTftpManager::RetrieveTftpClients","RetrieveTftpClients","RetrieveTftpClients method [Windows Deployment Services]","RetrieveTftpClients method [Windows Deployment Services]","IWdsTransportTftpManager interface","wds.iwdstransporttftpclient_retrievetftpclients","wdstptmgmt/IWdsTransportTftpManager::RetrieveTftpClients"]
old-location: wds\iwdstransporttftpclient_retrievetftpclients.htm
tech.root: wds
ms.assetid: 48527950-A29D-4BC0-AD85-7B40E9C19133
ms.date: 12/05/2018
ms.keywords: IWdsTransportTftpManager interface [Windows Deployment Services],RetrieveTftpClients method, IWdsTransportTftpManager.RetrieveTftpClients, IWdsTransportTftpManager::RetrieveTftpClients, RetrieveTftpClients, RetrieveTftpClients method [Windows Deployment Services], RetrieveTftpClients method [Windows Deployment Services],IWdsTransportTftpManager interface, wds.iwdstransporttftpclient_retrievetftpclients, wdstptmgmt/IWdsTransportTftpManager::RetrieveTftpClients
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWdsTransportTftpManager::RetrieveTftpClients
 - wdstptmgmt/IWdsTransportTftpManager::RetrieveTftpClients
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportTftpManager.RetrieveTftpClients
---

# IWdsTransportTftpManager::RetrieveTftpClients


## -description

Returns a pointer to the object of an <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a> interface containing a collection of objects of the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransporttftpclient">IWdsTransportTftpClient</a> interface for the clients currently connected to the TFTP server.

## -parameters

### -param ppWdsTransportTftpClients [out, retval]

A pointer to a pointer to an object of the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a> interface.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransporttftpmanager">IWdsTransportTftpManager</a>