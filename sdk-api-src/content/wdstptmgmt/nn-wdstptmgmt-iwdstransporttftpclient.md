---
UID: NN:wdstptmgmt.IWdsTransportTftpClient
title: IWdsTransportTftpClient (wdstptmgmt.h)
description: This interface is used to specify information of a TFTP client session currently active in the server.
helpviewer_keywords: ["IWdsTransportTftpClient","IWdsTransportTftpClient interface [Windows Deployment Services]","IWdsTransportTftpClient interface [Windows Deployment Services]","described","wds.iwdstransporttftpclient","wdstptmgmt/IWdsTransportTftpClient"]
old-location: wds\iwdstransporttftpclient.htm
tech.root: wds
ms.assetid: B612A719-247E-40CC-B7BC-E2A6144DA329
ms.date: 12/05/2018
ms.keywords: IWdsTransportTftpClient, IWdsTransportTftpClient interface [Windows Deployment Services], IWdsTransportTftpClient interface [Windows Deployment Services],described, wds.iwdstransporttftpclient, wdstptmgmt/IWdsTransportTftpClient
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
 - IWdsTransportTftpClient
 - wdstptmgmt/IWdsTransportTftpClient
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
 - IWdsTransportTftpClient
---

# IWdsTransportTftpClient interface


## -description

This interface is used to specify information of a TFTP client session currently active in the server.  A collection of objects of the <b>IWdsTransportTftpClient</b> interface can be obtained using the <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransporttftpmanager-retrievetftpclients">IWdsTransportTftpManager::RetrieveTftpClients</a> method.