---
UID: NN:mswmdm.IWMDMProgress
title: IWMDMProgress (mswmdm.h)
author: windows-sdk-content
description: The optional, application-implemented IWMDMProgress allows an application to track the progress of operations, such as formatting media or file transfers.
old-location: wmdm\iwmdmprogress.htm
tech.root: WMDM
ms.assetid: 9af022a6-19b4-41b7-b951-0acad6aab4a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMProgress, IWMDMProgress interface [windows Media Device Manager], IWMDMProgress interface [windows Media Device Manager],described, IWMDMProgressInterface, mswmdm/IWMDMProgress, wmdm.iwmdmprogress
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMProgress"
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMProgress interface


## -description



The optional, application-implemented <b>IWMDMProgress</b> allows an application to track the progress of operations, such as formatting media or file transfers. This interface is submitted to, and called by, the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl</a> interfaces.

These methods do not provide a way for the application to know which operation is being tracked. However, the <b>IWMDMProgress3</b> methods do provide a means to identify the operation; if possible, you should implement that interface instead.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMProgress</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-begin">Begin</a>
</td>
<td align="left" width="63%">
Indicates that an operation is beginning. An estimate of the duration of the operation is provided when possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end">End</a>
</td>
<td align="left" width="63%">
Indicates that an operation is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-progress">Progress</a>
</td>
<td align="left" width="63%">
Indicates that an operation is still in progress.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2">IWMDMProgress2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

