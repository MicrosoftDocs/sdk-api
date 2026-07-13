---
UID: NF:clusapi.ClusterRegOpenKey
title: ClusterRegOpenKey function (clusapi.h)
description: Opens an existing cluster database key.
helpviewer_keywords: ["ClusterRegOpenKey","ClusterRegOpenKey function [Failover Cluster]","_wolf_clusterregopenkey","clusapi/ClusterRegOpenKey","mscs.clusterregopenkey"]
old-location: mscs\clusterregopenkey.htm
tech.root: MsCS
ms.assetid: f2cf204e-d02d-40b9-86d7-0262b8cc4db1
ms.date: 12/05/2018
ms.keywords: ClusterRegOpenKey, ClusterRegOpenKey function [Failover Cluster], _wolf_clusterregopenkey, clusapi/ClusterRegOpenKey, mscs.clusterregopenkey
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegOpenKey
 - clusapi/ClusterRegOpenKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterRegOpenKey
---

# ClusterRegOpenKey function


## -description

Opens an existing  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

Handle to a currently open key. This parameter cannot be <b>NULL</b>.

### -param lpszSubKey [in]

Pointer to a null-terminated Unicode string specifying the name of the subkey to be created or opened. The <i>lpszSubKey</i> parameter must point to a subkey that:

<ul>
<li>Is a child key of the key identified by <i>hKey</i>.</li>
<li>Must not begin with the backslash character ( \ ).</li>
<li>Must not be <b>NULL</b>.</li>
</ul>
The <i>lpszSubKey</i> parameter can point to an empty string, causing  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatekey">ClusterRegCreateKey</a> to return a handle to the database key represented by <i>hKey</i>.

### -param samDesired [in]

Access mask that specifies the security access needed for the new key.

### -param phkResult [out]

Pointer to a handle to the opened or created key.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Callers should call  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close the key handle opened by  <b>ClusterRegOpenKey</b> when they are done with it.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatekey">ClusterRegCreateKey</a>