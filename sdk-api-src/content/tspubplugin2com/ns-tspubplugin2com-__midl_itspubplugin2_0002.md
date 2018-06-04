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

# __MIDL_ItsPubPlugin2_0002 structure


## -description


Contains additional information about a resource that can be assigned to users in RemoteApp and Desktop Connection.


## -struct-fields




### -field resourceV1

A <a href="https://msdn.microsoft.com/209dee74-c52e-4e31-9d1b-1e7c6c0d0121">pluginResource</a> structure that contains the basic information about the resource.


### -field pceFileAssocListSize

Reserved for future use. This member must be zero.


### -field fileAssocList

Reserved for future use. This member must be <b>NULL</b>.


### -field securityDescriptor

A string representation of a security descriptor used to specify the domain users and groups that have access to the resource. For more information about security descriptor strings, see <a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>.


### -field pceFolderListSize

The number of strings in the <b>folderList</b> array.


### -field folderList

An array of pointers to null-terminated strings that contain the names of the folders that the resource should be displayed in. You must use the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function to allocate these strings. The caller is responsible for freeing these strings.


## -remarks



The <b>pluginFolderName</b> type is defined as follows:

<code>typedef [string] WCHAR* pluginFolderName;</code>




## -see-also




<a href="https://msdn.microsoft.com/8edb3f28-0796-478e-bf0a-b157e1e12dc2">GetResource2</a>



<a href="https://msdn.microsoft.com/58b30088-be32-4aa0-88a4-459df52db7af">GetResource2List</a>



<a href="https://msdn.microsoft.com/209dee74-c52e-4e31-9d1b-1e7c6c0d0121">pluginResource</a>
 

 

