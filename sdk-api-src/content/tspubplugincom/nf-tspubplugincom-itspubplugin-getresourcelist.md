---
UID: NF:tspubplugincom.ItsPubPlugin.GetResourceList
title: ItsPubPlugin::GetResourceList (tspubplugincom.h)
description: Retrieves a list of resources assigned to the specified user. (ItsPubPlugin.GetResourceList)
helpviewer_keywords: ["GetResourceList","GetResourceList method [Remote Desktop Services]","GetResourceList method [Remote Desktop Services]","ItsPubPlugin interface","ItsPubPlugin interface [Remote Desktop Services]","GetResourceList method","ItsPubPlugin.GetResourceList","ItsPubPlugin::GetResourceList","termserv.itspubplugin_getresourcelist","tspubplugincom/ItsPubPlugin::GetResourceList"]
old-location: termserv\itspubplugin_getresourcelist.htm
tech.root: TermServ
ms.assetid: c8f255fe-6f31-4cbb-a600-a27e977a84a0
ms.date: 12/05/2018
ms.keywords: GetResourceList, GetResourceList method [Remote Desktop Services], GetResourceList method [Remote Desktop Services],ItsPubPlugin interface, ItsPubPlugin interface [Remote Desktop Services],GetResourceList method, ItsPubPlugin.GetResourceList, ItsPubPlugin::GetResourceList, termserv.itspubplugin_getresourcelist, tspubplugincom/ItsPubPlugin::GetResourceList
req.header: tspubplugincom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Cpubplugin.idl
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
 - ItsPubPlugin::GetResourceList
 - tspubplugincom/ItsPubPlugin::GetResourceList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tspubplugincom.h
api_name:
 - ItsPubPlugin.GetResourceList
---

# ItsPubPlugin::GetResourceList


## -description

Retrieves a list of resources assigned to the specified user. The RemoteApp and Desktop Connection Management service calls this method in the following situations:
<ul>
<li>When the user has no cache in Remote Desktop Web Access (RD Web Access).</li>
<li>When the user has a cache, but it has expired.</li>
<li>When a call to <a href="/windows/desktop/api/tspubplugincom/nf-tspubplugincom-itspubplugin-getcachelastupdatetime">GetCacheLastUpdateTime</a> returns a time that is later than the time stored in the user's cache.</li>
</ul>

## -parameters

### -param userID [in]

The user security identifier (SID).

### -param pceAppListSize [out]

A pointer to a <b>LONG</b> variable to receive the number of elements in the <i>resourceList</i>.

### -param resourceList [out]

The address of a pointer to an array of <a href="/windows/win32/api/tspubplugincom/ns-tspubplugincom-pluginresource">pluginResource</a> structures that receive the resources assigned to the specified user. You must use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function to allocate this memory. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin">ItsPubPlugin</a>
