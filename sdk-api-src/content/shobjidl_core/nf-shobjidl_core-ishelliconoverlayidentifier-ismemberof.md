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

# IShellIconOverlayIdentifier::IsMemberOf


## -description


Specifies whether an icon overlay should be added to a Shell object's icon.


## -parameters




### -param pwszPath [in]

Type: <b>PCWSTR</b>

A Unicode string that contains the fully qualified path of the Shell object.


### -param dwAttrib

Type: <b>DWORD</b>

The object's attributes. For a complete list of file attributes and their associated flags, see <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>.


## -returns



Type: <b>HRESULT</b>

This method returns one of the following:

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
The icon overlay should be displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The icon overlay should not be displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>
 




## -remarks



The Shell calls this method to determine whether it should display a handler's icon overlay for a particular object. Icon overlay handlers are usually intended to work with a particular group of files. A typical example is a <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">file type</a>, identified by a specific file name extension. An icon overlay handler might request an icon overlay for all members of the file type. Some handlers request an icon overlay only if a member of the file type is in a particular state. However, icon overlay handlers are free to request their icon overlay for any object that they want.




## -see-also




<a href="https://msdn.microsoft.com/c093bc13-def7-411d-b741-50996ffad84b">IShellIconOverlayIdentifier</a>
 

 

