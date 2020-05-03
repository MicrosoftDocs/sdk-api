---
UID: NN:mswmdm.IWMDMProgress3
title: IWMDMProgress3 (mswmdm.h)
description: The optional, application-implemented IWMDMProgress3 interface extends IWMDMProgress2 by providing additional input parameters to specify which event is being monitored, and to allow for context-specific information.Applications that implement this callback interface should provide an implementation for methods corresponding to IWMDMProgress and IWMDMProgress2 for backward compatibility, in addition to the new methods.helpviewer_keywords: ["IWMDMProgress3","IWMDMProgress3 interface [windows Media Device Manager]","IWMDMProgress3 interface [windows Media Device Manager]","described","IWMDMProgress3Interface","mswmdm/IWMDMProgress3","wmdm.iwmdmprogress3"]
old-location: wmdm\iwmdmprogress3.htm
tech.root: WMDM
ms.assetid: fc3a7031-ac1b-45cf-889b-2d40d50b347d
ms.date: 12/05/2018
ms.keywords: IWMDMProgress3, IWMDMProgress3 interface [windows Media Device Manager], IWMDMProgress3 interface [windows Media Device Manager],described, IWMDMProgress3Interface, mswmdm/IWMDMProgress3, wmdm.iwmdmprogress3
f1_keywords:
- mswmdm/IWMDMProgress3
dev_langs:
- c++
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
- IWMDMProgress3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMProgress3 interface


## -description



The optional, application-implemented <b>IWMDMProgress3</b> interface extends <b>IWMDMProgress2</b> by providing additional input parameters to specify which event is being monitored, and to allow for context-specific information.

Applications that implement this callback interface should provide an implementation for methods corresponding to <b>IWMDMProgress</b> and <b>IWMDMProgress2</b> for backward compatibility, in addition to the new methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMProgress3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a>. <b>IWMDMProgress3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMProgress3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-begin3">Begin3</a>
</td>
<td align="left" width="63%">
Indicates that an operation is about to begin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">End3</a>
</td>
<td align="left" width="63%">
Indicates that an operation is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-progress3">Progress3</a>
</td>
<td align="left" width="63%">
Indicates the status of an action in progress.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2">IWMDMProgress2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

