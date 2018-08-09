---
UID: NN:wdstptmgmt.IWdsTransportTftpClient
title: IWdsTransportTftpClient
author: windows-sdk-content
description: This interface is used to specify information of a TFTP client session currently active in the server.
old-location: wds\iwdstransporttftpclient.htm
old-project: wds
ms.assetid: B612A719-247E-40CC-B7BC-E2A6144DA329
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWdsTransportTftpClient, IWdsTransportTftpClient interface [Windows Deployment Services], IWdsTransportTftpClient interface [Windows Deployment Services],described, wds.iwdstransporttftpclient, wdstptmgmt/IWdsTransportTftpClient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportTftpClient
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportTftpClient interface


## -description


This interface is used to specify information of a TFTP client session currently active in the server.  A collection of objects of the <b>IWdsTransportTftpClient</b> interface can be obtained using the <a href="https://msdn.microsoft.com/48527950-A29D-4BC0-AD85-7B40E9C19133">IWdsTransportTftpManager::RetrieveTftpClients</a> method.

