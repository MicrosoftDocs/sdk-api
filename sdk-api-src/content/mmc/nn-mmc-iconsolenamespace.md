---
UID: NN:mmc.IConsoleNameSpace
title: IConsoleNameSpace (mmc.h)
author: windows-sdk-content
description: Enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer.
old-location: mmc\iconsolenamespace.htm
tech.root: mmc
ms.assetid: 0E72A4DF-5A74-49DD-BD94-06860EFFE09A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConsoleNameSpace, IConsoleNameSpace interface [MMC], IConsoleNameSpace interface [MMC],described, mmc.iconsolenamespace, mmc/IConsoleNameSpace
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
 - IConsoleNameSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConsoleNameSpace interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer. For example, a snap-in that features a domain object might enumerate individual groups or organizations within the domain.

The snap-in can query for a pointer to the 
<b>IConsoleNameSpace</b> interface during a call to its 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-initialize">IComponentData::Initialize</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsoleNameSpace</b> interface inherits from <b>IConsoleNameSpace</b>. <b>IConsoleNameSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsoleNameSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-deleteitem">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item from the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">GetChildItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the first child item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/lwef/-search-2x-ipropertyfiltercollection-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the attributes of a single scope pane item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getnextitem">GetNextItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the next item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/wia/-wia-iwiaitem2-getparentitem">GetParentItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the parent item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/dotnet/api/microsoft.clradmin.iconsolenamespace2.insertitem">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item into the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setitem">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the attributes of a single scope pane item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-interfaces-and-methods">MMC 2.0 Interfaces and Methods</a>
 

 

