---
UID: NS:tspubplugin2com.__MIDL_ItsPubPlugin2_0002
title: pluginResource2 (tspubplugin2com.h)
description: Contains additional information about a resource that can be assigned to users in RemoteApp and Desktop Connection.
helpviewer_keywords: ["pluginResource2","pluginResource2 structure [Remote Desktop Services]","termserv.pluginresource2","tspubplugin2com/pluginResource2"]
old-location: termserv\pluginresource2.htm
tech.root: TermServ
ms.assetid: BD4761C7-377C-499C-B984-3B126C704089
ms.date: 12/05/2018
ms.keywords: pluginResource2, pluginResource2 structure [Remote Desktop Services], termserv.pluginresource2, tspubplugin2com/pluginResource2
req.header: tspubplugin2com.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tspubplugin2com.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: pluginResource2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_ItsPubPlugin2_0002
 - tspubplugin2com/__MIDL_ItsPubPlugin2_0002
 - pluginResource2
 - tspubplugin2com/pluginResource2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tspubplugin2com.h
api_name:
 - pluginResource2
---

# pluginResource2 structure


## -description

Contains additional information about a resource that can be assigned to users in RemoteApp and Desktop Connection.

## -struct-fields

### -field resourceV1

A <a href="/windows/win32/api/tspubplugincom/ns-tspubplugincom-pluginresource">pluginResource</a> structure that contains the basic information about the resource.

### -field pceFileAssocListSize

Reserved for future use. This member must be zero.

### -field fileAssocList

Reserved for future use. This member must be <b>NULL</b>.

### -field securityDescriptor

A string representation of a security descriptor used to specify the domain users and groups that have access to the resource. For more information about security descriptor strings, see <a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor String Format</a>.

### -field pceFolderListSize

The number of strings in the <b>folderList</b> array.

### -field folderList

An array of pointers to null-terminated strings that contain the names of the folders that the resource should be displayed in. You must use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function to allocate these strings. The caller is responsible for freeing these strings.

## -remarks

The <b>pluginFolderName</b> type is defined as follows:

<code>typedef [string] WCHAR* pluginFolderName;</code>

## -see-also

<a href="/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-getresource2">GetResource2</a>



<a href="/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-getresource2list">GetResource2List</a>



<a href="/windows/win32/api/tspubplugincom/ns-tspubplugincom-pluginresource">pluginResource</a>