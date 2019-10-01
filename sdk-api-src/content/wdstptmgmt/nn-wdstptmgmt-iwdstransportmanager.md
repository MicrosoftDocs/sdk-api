---
UID: NN:wdstptmgmt.IWdsTransportManager
title: IWdsTransportManager (wdstptmgmt.h)
author: windows-sdk-content
description: Manages a WDS transport server. This is the top-level interface into the Windows Deployment Services (WDS) Transport Management API and the only interface that can be created using the CoCreateInstance function.
old-location: wds\iwdstransportmanager.htm
tech.root: wds
ms.assetid: 23f36ec7-5f6f-486c-bb09-e2f5b6f57efa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWdsTransportManager, IWdsTransportManager interface [Windows Deployment Services], IWdsTransportManager interface [Windows Deployment Services],described, wds.iwdstransportmanager, wdstptmgmt/IWdsTransportManager
ms.topic: interface
f1_keywords: 
 - "wdstptmgmt/IWdsTransportManager"
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
 - IWdsTransportManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportManager interface


## -description


Manages a WDS transport server. This is the top-level interface into the Windows Deployment Services (WDS) Transport Management API and the only interface that can be created using the <b>CoCreateInstance</b> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWdsTransportManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportmanager-getwdstransportserver">GetWdsTransportServer</a>
</td>
<td align="left" width="63%">
Creates an object of the <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportserver">IWdsTransportServer</a> interface that can be used to manage a WDS transport server.

</td>
</tr>
</table> 

