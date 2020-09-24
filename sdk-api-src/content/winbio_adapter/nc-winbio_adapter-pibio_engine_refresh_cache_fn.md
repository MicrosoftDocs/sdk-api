---
UID: NC:winbio_adapter.PIBIO_ENGINE_REFRESH_CACHE_FN
title: PIBIO_ENGINE_REFRESH_CACHE_FN (winbio_adapter.h)
description: Notifies the Engine Adapter that it should discard any cached templates that it may be keeping in memory.
helpviewer_keywords: ["EngineAdapterRefreshCache","EngineAdapterRefreshCache callback function [Windows Biometric Framework API]","PIBIO_ENGINE_REFRESH_CACHE_FN","PIBIO_ENGINE_REFRESH_CACHE_FN callback","secbiomet.engineadapterrefreshcache","winbio_adapter/EngineAdapterRefreshCache"]
old-location: secbiomet\engineadapterrefreshcache.htm
tech.root: SecBioMet
ms.assetid: AD0A3BBC-3948-402A-AC3A-96BAF00A164C
ms.date: 12/05/2018
ms.keywords: EngineAdapterRefreshCache, EngineAdapterRefreshCache callback function [Windows Biometric Framework API], PIBIO_ENGINE_REFRESH_CACHE_FN, PIBIO_ENGINE_REFRESH_CACHE_FN callback, secbiomet.engineadapterrefreshcache, winbio_adapter/EngineAdapterRefreshCache
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - PIBIO_ENGINE_REFRESH_CACHE_FN
 - winbio_adapter/PIBIO_ENGINE_REFRESH_CACHE_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterRefreshCache
---

# PIBIO_ENGINE_REFRESH_CACHE_FN callback function


## -description

Called by the Windows Biometric Framework to notify the Engine Adapter that it should discard any cached templates that it may be keeping in memory.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

## -returns

The function will return one of the following <b>HRESULT</b> values. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
This value is returned in all other cases.

</td>
</tr>
</table>

## -remarks

An Engine Adapter that maintains a private in-memory cache of templates (e.g., for performance reasons) should discard the contents of its cache when it receives this method call. The call indicates that the cache contents are no longer valid. Depending on the Engine Adapter’s cache policy, the adapter may also choose to reload its cache at this time from the template database.

The biometric service calls this method in the following situations:<ul>
<li>
Once, when the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn">StorageAdapterAttach</a> routine has successfully opened its connection to the template database.

</li>
<li>
Again, after performing any operation that changes the state of the template database. <ul>
<li>
Adding a new template to the database.

</li>
<li>
Deleting one or more existing templates from the database.

</li>
</ul>


</li>
</ul>