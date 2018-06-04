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

# IShellMenu::GetShellFolder


## -description


Gets the folder that the menu band is set to browse.


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns successfully, contains a pointer to a set of flag values that specify how the menu band operates.


Can return any of the following flags.



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
 


Always returns one of the following flags.



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
 


### -param ppidl




### -param riid [in]

Type: <b>REFIID</b>

The REFIID for the target folder.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the address of a pointer to the Shell folder object referenced by the <i>riid</i>.


#### - pidlFolder [out]

Type: <b>PCIDLIST_ABSOLUTE*</b>

When this method returns, contains the address of the folder's fully qualified <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



