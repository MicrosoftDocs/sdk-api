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
 

 

