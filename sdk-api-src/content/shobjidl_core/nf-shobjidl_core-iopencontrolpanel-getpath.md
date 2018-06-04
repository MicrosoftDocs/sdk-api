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

# IOpenControlPanel::GetPath


## -description


Gets the path of a specified Control Panel item.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the item's canonical name or its <b>GUID</b>. This value can be <b>NULL</b>. See Remarks for further details. For a complete list of Control Panel item canonical names, see <a href="https://msdn.microsoft.com/A02DFC9F-646D-40d8-901C-7239A820DE2C">Canonical Names of Control Panel Items</a>.


### -param pszPath [out]

Type: <b>LPWSTR</b>

When this method returns, contains the path of the specified Control Panel item as a Unicode string.


### -param cchPath [in]

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszPath</i>, in WCHARs.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>pszName</i> points to the item's canonical name or <b>GUID</b>, then the path returned is in one of these two forms, depending on the most recent Control Panel view (Classic View or Category View):

                

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>::{CLSID_ControlPanel}\::{item guid}
::{CLSID_ControlPanelCategory}\categoryId\::{item guid}
</pre>
</td>
</tr>
</table></span></div>

                
                If <i>pszName</i> is <b>NULL</b> then one of these two values is returned:

                

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>::{CLSID_ControlPanel}
::{CLSID_ControlPanelCategory}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="ffd6c6de-2c65-4ab1-b1fa-27abe6a10342">Developing for the Control Panel</a>



<a href="https://msdn.microsoft.com/fbf86553-7aa1-4a0f-9775-5f71f41b1705">IOpenControlPanel</a>
 

 

