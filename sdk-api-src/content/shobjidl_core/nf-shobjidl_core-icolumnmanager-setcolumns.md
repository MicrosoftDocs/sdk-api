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

# IColumnManager::SetColumns


## -description


Sets the collection of columns for the view to display.


## -parameters




### -param rgkeyOrder [in]

Type: <b>const <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures that specify the columns to display.


### -param cVisible [in]

Type: <b>UINT</b>

The size of the <i>rgkeyOrder</i> array.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Collection set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>failure</b></dt>
</dl>
</td>
<td width="60%">
Collection not set.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  <b>IColumnManager::SetColumns</b> clears the state of all columns, so <a href="https://msdn.microsoft.com/3a52d634-0ff0-4dbc-81cb-90cdffe4f6ae">IColumnManager::SetColumnInfo</a> must be called afterward to set the state of individual columns.</div>
<div> </div>


