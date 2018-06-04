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

# IColumnManager::GetColumnInfo


## -description


Gets information about each column: width, visibility, display name, and state.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param pcmci [in, out]

Type: <b><a href="https://msdn.microsoft.com/b4437aa7-9682-4819-a353-936179e84005">CM_COLUMNINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/b4437aa7-9682-4819-a353-936179e84005">CM_COLUMNINFO</a> structure. On entry, set this structure's <b>dwMask</b> member to specify the information to retrieve. Also set its <b>cbSize</b> member. When this method returns successfully, the structure contains the requested information.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

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
Column information obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>failure</b></dt>
</dl>
</td>
<td width="60%">
Column information not obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that cbSize member of <i>pcmci</i> does not equal the size of CM_COLUMNINFO.

</td>
</tr>
</table>
 



