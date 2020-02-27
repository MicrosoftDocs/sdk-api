---
UID: NN:wdstptmgmt.IWdsTransportTftpManager
title: IWdsTransportTftpManager (wdstptmgmt.h)
description: This interface provides a method to retrieve all the clients currently connected to the TFTP server.
old-location: wds\iwdstransporttftpmanager.htm
tech.root: wds
ms.assetid: A2DB8313-2855-4B0E-908E-CAE71E88FEF0
ms.date: 12/05/2018
ms.keywords: IWdsTransportTftpManager, IWdsTransportTftpManager interface [Windows Deployment Services], IWdsTransportTftpManager interface [Windows Deployment Services],described, wds.iwdstransporttftpmanager, wdstptmgmt/IWdsTransportTftpManager
f1_keywords:
- wdstptmgmt/IWdsTransportTftpManager
dev_langs:
- c++
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
- IWdsTransportTftpManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportTftpManager interface


## -description


This interface provides a method to retrieve all the clients currently connected to the TFTP server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportTftpManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportTftpManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransporttftpmanager-retrievetftpclients">RetrieveTftpClients</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object of an <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportcollection">IWdsTransportCollection</a> interface containing a collection of objects of the <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransporttftpclient">IWdsTransportTftpClient</a> interface for the clients currently connected to the TFTP server. 

</td>
</tr>
</table> 

