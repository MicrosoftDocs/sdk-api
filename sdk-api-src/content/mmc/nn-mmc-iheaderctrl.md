---
UID: NN:mmc.IHeaderCtrl
title: IHeaderCtrl (mmc.h)
description: Enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.helpviewer_keywords: ["IHeaderCtrl","IHeaderCtrl interface [MMC]","IHeaderCtrl interface [MMC]","described","mmc.iheaderctrl","mmc/IHeaderCtrl"]
old-location: mmc\iheaderctrl.htm
tech.root: mmc
ms.assetid: 8F7ACE7E-4B44-448A-A3BB-4563DDC9C34E
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl, IHeaderCtrl interface [MMC], IHeaderCtrl interface [MMC],described, mmc.iheaderctrl, mmc/IHeaderCtrl
f1_keywords:
- mmc/IHeaderCtrl
dev_langs:
- c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmcndmgr.dll
api_name:
- IHeaderCtrl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHeaderCtrl interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.

These methods provide support for users to filter list views based on filters set on each column in the result view. Be aware that a return value of <b>E_NOTIMPL</b> by any one of these methods indicates that list view filtering is not available in the version of MMC in which the snap-in is loaded.

The 
<b>IHeaderCtrl</b> interface can be queried from the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a> interface passed into 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">IComponent::Initialize</a> during the component's creation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHeaderCtrl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHeaderCtrl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHeaderCtrl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iheaderctrl-deletecolumn">DeleteColumn</a>
</td>
<td align="left" width="63%">
Removes a column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iheaderctrl-getcolumntext">GetColumnText</a>
</td>
<td align="left" width="63%">
Retrieves the text from a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iheaderctrl-getcolumnwidth">GetColumnWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iheaderctrl-insertcolumn">InsertColumn</a>
</td>
<td align="left" width="63%">
Adds a column to a default result view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iheaderctrl-setcolumntext">SetColumnText</a>
</td>
<td align="left" width="63%">
Sets the text in a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iheaderctrl-setcolumnwidth">SetColumnWidth</a>
</td>
<td align="left" width="63%">
Sets the width of a specified column.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-interfaces-and-methods">MMC 2.0 Interfaces and Methods</a>
 

 

