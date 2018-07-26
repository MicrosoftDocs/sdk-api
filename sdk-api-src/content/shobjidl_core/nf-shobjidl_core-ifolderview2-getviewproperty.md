---
UID: NF:shobjidl_core.IFolderView2.GetViewProperty
title: IFolderView2::GetViewProperty
author: windows-sdk-content
description: Gets a property value for a given property key from the view's cache.
old-location: shell\IFolderView2_GetViewProperty.htm
old-project: shell
ms.assetid: 26749aa8-9c5d-4b6b-b5af-bf52d4e8c8ce
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: GetViewProperty, GetViewProperty method [Windows Shell], GetViewProperty method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetViewProperty method, IFolderView2.GetViewProperty, IFolderView2::GetViewProperty, _shell_IFolderView2_GetViewProperty, shell.IFolderView2_GetViewProperty, shobjidl_core/IFolderView2::GetViewProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.GetViewProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView2::GetViewProperty


## -description


<p class="CCE_Message">[This method is still implemented, but should be considered deprecated as of Windows 7. It might not be implemented in future versions of Windows. It cannot be used with items in search results or library views, so consider using the item's existing properties or, if applicable, emitting properties from your namespace or property handler. See <a href="https://msdn.microsoft.com/library/Bb266532(v=VS.85).aspx">Developing Property Handlers for Windows Search</a> for more information.]

Gets a property value for a given property key from the view's cache.
	
            


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an item identifier list (PIDL).


### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> to be retrieved.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure in which the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> is stored.


## -returns



Type: <b>DEPRECATED_HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

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
Success, the value is in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The value is not in the view's cache.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/52fcf0df-f532-4114-b1c9-96838f1a5e77">IFolderView2</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>



<a href="https://msdn.microsoft.com/b7af0491-2ece-42b5-8eea-32643854632f">Property Lists</a>
 

 

