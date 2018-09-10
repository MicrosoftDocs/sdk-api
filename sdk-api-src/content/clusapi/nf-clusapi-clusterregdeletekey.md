---
UID: NF:clusapi.ClusterRegDeleteKey
title: ClusterRegDeleteKey function
author: windows-sdk-content
description: Deletes a cluster database key.
old-location: mscs\clusterregdeletekey.htm
tech.root: mscs
ms.assetid: af2b3b9c-2ff1-483e-a9cf-5db7b1fcbd85
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClusterRegDeleteKey, ClusterRegDeleteKey function [Failover Cluster], _wolf_clusterregdeletekey, clusapi/ClusterRegDeleteKey, mscs.clusterregdeletekey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegDeleteKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegDeleteKey function


## -description


Deletes a <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle to a currently open key.


### -param lpszSubKey [in]

Pointer to a null-terminated Unicode string specifying the name of the key to delete. The key pointed to by 
      <i>lpszSubKey</i> cannot have subkeys; 
      <b>ClusterRegDeleteKey</b> can only delete keys without 
      subkeys. This parameter cannot be <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The <b>ClusterRegDeleteKey</b> function cannot delete 
    a key that has one or more subkeys.

Do not call <b>ClusterRegDeleteKey</b> from the 
    following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/c7c74440-c98a-4440-8bf4-10ebd1a68608">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>
<b>ClusterRegDeleteKey</b> can be safely called from 
    any other resource DLL entry point function or from a worker thread. For more information, see 
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/a5e924bd-9336-45c8-b2c9-48291f8db774">ClusterRegCreateKey</a>
 

 

