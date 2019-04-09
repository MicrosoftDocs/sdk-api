---
UID: NN:mmc.IHeaderCtrl
title: IHeaderCtrl (mmc.h)
author: windows-sdk-content
description: Enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.
old-location: mmc\iheaderctrl.htm
tech.root: mmc
ms.assetid: 8F7ACE7E-4B44-448A-A3BB-4563DDC9C34E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl, IHeaderCtrl interface [MMC], IHeaderCtrl interface [MMC],described, mmc.iheaderctrl, mmc/IHeaderCtrl
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHeaderCtrl interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.

These methods provide support for users to filter list views based on filters set on each column in the result view. Be aware that a return value of <b>E_NOTIMPL</b> by any one of these methods indicates that list view filtering is not available in the version of MMC in which the snap-in is loaded.

The 
<b>IHeaderCtrl</b> interface can be queried from the 
<a href="https://msdn.microsoft.com/en-us/library/Mt300830(v=VS.85).aspx">IConsole</a> interface passed into 
<a href="https://msdn.microsoft.com/2a8b8f79-05c0-49e8-8210-7c1002ee5978">IComponent::Initialize</a> during the component's creation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHeaderCtrl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHeaderCtrl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2984b191-7a42-4778-b7a6-540d006253be">DeleteColumn</a>
</td>
<td align="left" width="63%">
Removes a column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f72c971-510a-4221-b14b-7a6b93b832bf">GetColumnText</a>
</td>
<td align="left" width="63%">
Retrieves the text from a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7db96a20-c864-4d05-b160-1c255ba2a40d">GetColumnWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F5499550-9460-4BF9-AF99-F4BDC7F32EBC">InsertColumn</a>
</td>
<td align="left" width="63%">
Adds a column to a default result view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/882ed195-3984-4eac-bb35-0d523574cd8d">SetColumnText</a>
</td>
<td align="left" width="63%">
Sets the text in a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1e26540-54c0-49e5-bc72-048c1ae0efc4">SetColumnWidth</a>
</td>
<td align="left" width="63%">
Sets the width of a specified column.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c95742a4-ae9b-40f3-8d88-c4955e5a3032">MMC 2.0 Interfaces and Methods</a>
 

 

