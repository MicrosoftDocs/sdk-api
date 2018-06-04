---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IShellMenu::Initialize


## -description


Initializes a menu band.


## -parameters




### -param psmc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/96bfdc52-bd4a-4345-8dd1-7e716a3d9811">IShellMenuCallback</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/96bfdc52-bd4a-4345-8dd1-7e716a3d9811">IShellMenuCallback</a> interface. This interface receives notifications from the menu. This value can be <b>NULL</b>.


### -param uId [in]

Type: <b>UINT</b>

The identifier of the selected menu item. Set this parameter to -1 for the menu itself.


### -param uIdAncestor [in]

Type: <b>UINT</b>


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that control how the menu operates.


A combination of the following option values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMINIT_DEFAULT"></a><a id="sminit_default"></a><dl>
<dt><b>SMINIT_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
No options.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_RESTRICT_DRAGDROP"></a><a id="sminit_restrict_dragdrop"></a><dl>
<dt><b>SMINIT_RESTRICT_DRAGDROP</b></dt>
</dl>
</td>
<td width="60%">
Do not allow drag-and-drop.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_TOPLEVEL"></a><a id="sminit_toplevel"></a><dl>
<dt><b>SMINIT_TOPLEVEL</b></dt>
</dl>
</td>
<td width="60%">
This is the top band.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_CACHED"></a><a id="sminit_cached"></a><dl>
<dt><b>SMINIT_CACHED</b></dt>
</dl>
</td>
<td width="60%">
Do not destroy the band when the window is closed.

</td>
</tr>
</table>
 


In addition to the values above, one of the following layout options:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMINIT_VERTICAL"></a><a id="sminit_vertical"></a><dl>
<dt><b>SMINIT_VERTICAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies a vertical band.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_HORIZONTAL"></a><a id="sminit_horizontal"></a><dl>
<dt><b>SMINIT_HORIZONTAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies a horizontal band.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



