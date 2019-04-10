---
UID: NN:shobjidl.INameSpaceTreeControl2
title: INameSpaceTreeControl2 (shobjidl.h)
author: windows-sdk-content
description: Extends the INameSpaceTreeControl interface by providing methods that get and set the display styles of treeview controls for use with Shell namespace items.
old-location: shell\INameSpaceTreeControl2.htm
tech.root: shell
ms.assetid: 5f9514db-35fe-44c7-9324-d69022628913
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl2, INameSpaceTreeControl2 interface [Windows Shell], INameSpaceTreeControl2 interface [Windows Shell],described, _shell_INameSpaceTreeControl2, shell.INameSpaceTreeControl2, shobjidl/INameSpaceTreeControl2
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl.h
api_name:
 - INameSpaceTreeControl2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControl2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> interface by providing methods that get and set the display styles of treeview controls for use with Shell namespace items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControl2</b> interface inherits from <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a>. <b>INameSpaceTreeControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INameSpaceTreeControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5305d7ba-e37f-4f95-8ae2-e0532012cb1e">GetControlStyle</a>
</td>
<td align="left" width="63%">
Gets the display styles set for the namespace object's treeview controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c96d936-2a79-491b-8e1e-2dd0e71aba10">GetControlStyle2</a>
</td>
<td align="left" width="63%">
Gets the extended display styles set for the namespace object's treeview controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20a212e2-13e8-4e17-a8d3-78fff2a1fafb">SetControlStyle</a>
</td>
<td align="left" width="63%">
Sets the display styles for the namespace object's treeview controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17d54fa9-ff5c-4fca-a7a6-7ecd4a58c7b9">SetControlStyle2</a>
</td>
<td align="left" width="63%">
Sets the extended display styles for the namespace object's treeview controls.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> interface, from which it inherits.

Use class identifier (CLSID) CLSID_NameSpaceTreeControl to instantiate an instance of this interface.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided with Windows. Third parties should not implement their own versions.



