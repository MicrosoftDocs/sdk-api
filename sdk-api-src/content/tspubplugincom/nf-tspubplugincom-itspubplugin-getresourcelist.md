---
UID: NF:tspubplugincom.ItsPubPlugin.GetResourceList
title: ItsPubPlugin::GetResourceList
author: windows-sdk-content
description: Retrieves a list of resources assigned to the specified user.
old-location: termserv\itspubplugin_getresourcelist.htm
tech.root: termserv
ms.assetid: c8f255fe-6f31-4cbb-a600-a27e977a84a0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetResourceList, GetResourceList method [Remote Desktop Services], GetResourceList method [Remote Desktop Services],ItsPubPlugin interface, ItsPubPlugin interface [Remote Desktop Services],GetResourceList method, ItsPubPlugin.GetResourceList, ItsPubPlugin::GetResourceList, termserv.itspubplugin_getresourcelist, tspubplugincom/ItsPubPlugin::GetResourceList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tspubplugincom.h
api_name:
 - ItsPubPlugin.GetResourceList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ItsPubPlugin::GetResourceList


## -description


Retrieves a list of resources assigned to the specified user. The RemoteApp and Desktop Connection Management service calls this method in the following situations:
<ul>
<li>When the user has no cache in Remote Desktop Web Access (RD Web Access).</li>
<li>When the user has a cache, but it has expired.</li>
<li>When a call to <a href="https://msdn.microsoft.com/66b18c7f-2623-44ed-8cb9-3cceaa9bab34">GetCacheLastUpdateTime</a> returns a time that is later than the time stored in the user's cache.</li>
</ul>

## -parameters




### -param userID [in]

The user security identifier (SID).


### -param pceAppListSize [out]

A pointer to a <b>LONG</b> variable to receive the number of elements in the <i>resourceList</i>. 


### -param resourceList [out]

The address of a pointer to an array of <a href="https://msdn.microsoft.com/209dee74-c52e-4e31-9d1b-1e7c6c0d0121">pluginResource</a> structures that receive the resources assigned to the specified user. You must use the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function to allocate this memory. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37d33f27-a811-4c97-bc80-ff8a5b8fcb7c">ItsPubPlugin</a>
 

 

