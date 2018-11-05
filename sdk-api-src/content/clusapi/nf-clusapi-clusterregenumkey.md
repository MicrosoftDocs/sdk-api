---
UID: NF:clusapi.ClusterRegEnumKey
title: ClusterRegEnumKey function
author: windows-sdk-content
description: Enumerates the subkeys of an open cluster database key.
old-location: mscs\clusterregenumkey.htm
tech.root: mscs
ms.assetid: ed70c16d-98d2-4d84-b5cd-1e5decc5b7bd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ClusterRegEnumKey, ClusterRegEnumKey function [Failover Cluster], _wolf_clusterregenumkey, clusapi/ClusterRegEnumKey, mscs.clusterregenumkey
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
 - ClusterRegEnumKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegEnumKey function


## -description


Enumerates the subkeys of an open 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key.


## -parameters




### -param hKey [in]

<b>HKEY</b> specifying a currently open key.


### -param dwIndex [in]

Index used to identify the next subkey to be enumerated. This parameter should be zero for the first call to 
       <b>ClusterRegEnumKey</b> and then incremented for 
       subsequent calls.

Because subkeys are not ordered, any new subkey has an arbitrary index. This means that 
       <b>ClusterRegEnumKey</b> may return subkeys in any 
       order.


### -param lpszName [out]

Pointer to a buffer that receives the name of the subkey, including the null-terminating character. The 
       function copies only the name of the subkey, not the full key hierarchy, to the buffer.


### -param lpcchName [in, out]

Pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


### -param lpftLastWriteTime [out, optional]

Pointer to the last time the enumerated subkey was modified.


## -returns



The function returns one of the following values.




## -remarks



The <b>ClusterRegEnumKey</b> function retrieves 
     information about one subkey each time it is called.

Because <b>ClusterRegEnumKey</b> enumerates keys from 
     the root of the database on the node on which the application is running when <i>hKey</i> is 
     set to <b>NULL</b>, 
     <b>ClusterRegEnumKey</b> fails if the node is not part of 
     a cluster.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/f2cf204e-d02d-40b9-86d7-0262b8cc4db1">ClusterRegOpenKey</a>
 

 

