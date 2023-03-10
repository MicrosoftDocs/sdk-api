---
UID: NF:tspubplugin2com.ItsPubPlugin2.GetResource2List
title: ItsPubPlugin2::GetResource2List (tspubplugin2com.h)
description: Retrieves a list of resources assigned to the specified user. (ItsPubPlugin2.GetResource2List)
helpviewer_keywords: ["GetResource2List","GetResource2List method [Remote Desktop Services]","GetResource2List method [Remote Desktop Services]","ItsPubPlugin2 interface","ItsPubPlugin2 interface [Remote Desktop Services]","GetResource2List method","ItsPubPlugin2.GetResource2List","ItsPubPlugin2::GetResource2List","termserv.itspubplugin2_getresource2list","tspubplugin2com/ItsPubPlugin2::GetResource2List"]
old-location: termserv\itspubplugin2_getresource2list.htm
tech.root: TermServ
ms.assetid: 58b30088-be32-4aa0-88a4-459df52db7af
ms.date: 12/05/2018
ms.keywords: GetResource2List, GetResource2List method [Remote Desktop Services], GetResource2List method [Remote Desktop Services],ItsPubPlugin2 interface, ItsPubPlugin2 interface [Remote Desktop Services],GetResource2List method, ItsPubPlugin2.GetResource2List, ItsPubPlugin2::GetResource2List, termserv.itspubplugin2_getresource2list, tspubplugin2com/ItsPubPlugin2::GetResource2List
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ItsPubPlugin2::GetResource2List
 - tspubplugin2com/ItsPubPlugin2::GetResource2List
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tspubplugin2com.h
api_name:
 - ItsPubPlugin2.GetResource2List
---

# ItsPubPlugin2::GetResource2List


## -description

Retrieves a list of resources assigned to the specified user. The RemoteApp and Desktop Connection Management service calls this method in the following situations:
<ul>
<li>When the user has no cache in Remote Desktop Web Access (RD Web Access).</li>
<li>When the user has a cache, but it has expired.</li>
<li>When a call to <a href="/windows/desktop/api/tspubplugincom/nf-tspubplugincom-itspubplugin-getcachelastupdatetime">GetCacheLastUpdateTime</a> returns a time that is later than the time stored in the user's cache.</li>
</ul>

## -parameters

### -param userID [in]

A null-terminated string that contains the security identifier (SID) of the user. If this parameter is <b>NULL</b>, this method should return the resources for all users.

### -param pceAppListSize [out]

The address of a <b>LONG</b> variable that receives the number of elements in the <i>resourceList</i> array.

### -param resourceList [out]

The address of an array of <a href="/windows/win32/api/tspubplugin2com/ns-tspubplugin2com-pluginresource2">pluginResource2</a> structures that contains the resources for the specified user. You must use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function to allocate this memory. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tspubplugin2com/nn-tspubplugin2com-itspubplugin2">ItsPubPlugin2</a>
