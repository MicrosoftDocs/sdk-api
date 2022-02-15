---
UID: NF:tspubplugincom.ItsPubPlugin.GetCacheLastUpdateTime
title: ItsPubPlugin::GetCacheLastUpdateTime (tspubplugincom.h)
description: Returns the time that the cache was last updated.
helpviewer_keywords: ["GetCacheLastUpdateTime","GetCacheLastUpdateTime method [Remote Desktop Services]","GetCacheLastUpdateTime method [Remote Desktop Services]","ItsPubPlugin interface","ItsPubPlugin interface [Remote Desktop Services]","GetCacheLastUpdateTime method","ItsPubPlugin.GetCacheLastUpdateTime","ItsPubPlugin::GetCacheLastUpdateTime","termserv.itspubplugin_getcachelastupdatetime","tspubplugincom/ItsPubPlugin::GetCacheLastUpdateTime"]
old-location: termserv\itspubplugin_getcachelastupdatetime.htm
tech.root: TermServ
ms.assetid: 66b18c7f-2623-44ed-8cb9-3cceaa9bab34
ms.date: 12/05/2018
ms.keywords: GetCacheLastUpdateTime, GetCacheLastUpdateTime method [Remote Desktop Services], GetCacheLastUpdateTime method [Remote Desktop Services],ItsPubPlugin interface, ItsPubPlugin interface [Remote Desktop Services],GetCacheLastUpdateTime method, ItsPubPlugin.GetCacheLastUpdateTime, ItsPubPlugin::GetCacheLastUpdateTime, termserv.itspubplugin_getcachelastupdatetime, tspubplugincom/ItsPubPlugin::GetCacheLastUpdateTime
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
 - ItsPubPlugin::GetCacheLastUpdateTime
 - tspubplugincom/ItsPubPlugin::GetCacheLastUpdateTime
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
 - ItsPubPlugin.GetCacheLastUpdateTime
---

# ItsPubPlugin::GetCacheLastUpdateTime


## -description

Returns the time that the cache was last updated. The RemoteApp and Desktop Connection Management service calls this method to determine whether the data in the Remote Desktop Web Access (RD Web Access) cache should be refreshed.

## -parameters

### -param lastUpdateTime [out]

A pointer to an  <b>unsigned long long</b> variable that receives the time that the cache was last updated.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The RemoteApp and Desktop Connection Management service calls this method to get the last time that the cache was refreshed. If your plug-in does not implement caching, return the current system time. This tells the service that it must call <a href="/windows/desktop/api/tspubplugincom/nf-tspubplugincom-itspubplugin-getresourcelist">GetResourceList</a> to get the current list of resources. We recommend implementing the plug-in with caching because caching reduces the number of calls the service must make to <b>GetResourceList</b>.

## -see-also

<a href="/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin">ItsPubPlugin</a>