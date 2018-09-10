---
UID: NN:mmc.IConsoleNameSpace
title: IConsoleNameSpace
author: windows-sdk-content
description: Enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer.
old-location: mmc\iconsolenamespace.htm
tech.root: mmc
ms.assetid: 0E72A4DF-5A74-49DD-BD94-06860EFFE09A
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IConsoleNameSpace, IConsoleNameSpace interface [MMC], IConsoleNameSpace interface [MMC],described, mmc.iconsolenamespace, mmc/IConsoleNameSpace
ms.prod: windows
ms.technology: windows-sdk
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
---

# IConsoleNameSpace interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer. For example, a snap-in that features a domain object might enumerate individual groups or organizations within the domain.

The snap-in can query for a pointer to the 
<b>IConsoleNameSpace</b> interface during a call to its 
<a href="https://msdn.microsoft.com/7893b3d6-f576-41cc-bbe5-2fcef7c327d7">IComponentData::Initialize</a> method.


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
<a href="https://msdn.microsoft.com/a3324e25-1bfa-4adb-b811-509daff3127c">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item from the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a6f5712-27ae-456b-9889-03c18910a317">GetChildItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the first child item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72c4cafb-f39b-4e37-b8f0-4f0867ac78f0">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the attributes of a single scope pane item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e4ada78-4e95-4053-a1ce-05368e70dba7">GetNextItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the next item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b32d9669-b71d-4ff3-8cc5-c22503773644">GetParentItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the parent item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64d7b53a-f5a7-4735-a54e-a62bff579ba9">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item into the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdcd5630-b29f-484a-a20a-af4328e721a5">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the attributes of a single scope pane item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/894f99a6-2189-458d-a50f-497930d4a9dd">IConsoleNameSpace2</a>



<a href="https://msdn.microsoft.com/c95742a4-ae9b-40f3-8d88-c4955e5a3032">MMC 2.0 Interfaces and Methods</a>
 

 

