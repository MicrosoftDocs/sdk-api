---
UID: NN:wdstptmgmt.IWdsTransportTftpManager
title: IWdsTransportTftpManager
author: windows-sdk-content
description: This interface provides a method to retrieve all the clients currently connected to the TFTP server.
old-location: wds\iwdstransporttftpmanager.htm
old-project: Wds
ms.assetid: A2DB8313-2855-4B0E-908E-CAE71E88FEF0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWdsTransportTftpManager, IWdsTransportTftpManager interface [Windows Deployment Services], IWdsTransportTftpManager interface [Windows Deployment Services],described, wds.iwdstransporttftpmanager, wdstptmgmt/IWdsTransportTftpManager
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
 - IWdsTransportTftpManager
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportTftpManager interface


## -description


This interface provides a method to retrieve all the clients currently connected to the TFTP server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportTftpManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWdsTransportTftpManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWdsTransportTftpManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48527950-A29D-4BC0-AD85-7B40E9C19133">RetrieveTftpClients</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object of an <a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a> interface containing a collection of objects of the <a href="https://msdn.microsoft.com/B612A719-247E-40CC-B7BC-E2A6144DA329">IWdsTransportTftpClient</a> interface for the clients currently connected to the TFTP server. 

</td>
</tr>
</table> 

