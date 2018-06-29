---
UID: NF:propsys.IPropertyDescription.GetDisplayName
title: IPropertyDescription::GetDisplayName
author: windows-sdk-content
description: Gets the display name of the property as it is shown in any UI.
old-location: properties\IPropertyDescription_GetDisplayName.htm
old-project: properties
ms.assetid: 54ee12a4-15fe-454b-8233-297e98bc8a22
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetDisplayName, GetDisplayName method [Windows Properties], GetDisplayName method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetDisplayName method, IPropertyDescription.GetDisplayName, IPropertyDescription::GetDisplayName, properties.IPropertyDescription_GetDisplayName, propsys/IPropertyDescription::GetDisplayName, shell.IPropertyDescription_GetDisplayName, shell_IPropertyDescription_GetDisplayName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.GetDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription::GetDisplayName


## -description


Gets the display name of the property as it is shown in any UI.


## -parameters




### -param ppszName






#### - ppszDisplayName [out]

Type: <b>LPWSTR*</b>

Contains the address of a pointer to the property's name as a null-terminated Unicode string.


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
Display name is obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppszDisplayName</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory allocation failed.

</td>
</tr>
</table>
 




## -remarks



The information retrieved by this method comes from the <i>singularLabel</i> and <i>pluralLabel</i> attributes of the <a href="https://msdn.microsoft.com/library/Bb773876(v=VS.85).aspx">labelInfo</a> element in the property's .propdesc file.

It is the responsibility of the calling application to use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the string referred to by <i>ppszDisplayName</i> when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

