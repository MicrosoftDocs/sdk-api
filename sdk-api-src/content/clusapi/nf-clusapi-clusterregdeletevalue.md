---
UID: NF:clusapi.ClusterRegDeleteValue
title: ClusterRegDeleteValue function
author: windows-sdk-content
description: Removes a named value from a cluster database key.
old-location: mscs\clusterregdeletevalue.htm
tech.root: mscs
ms.assetid: 81d2936e-6f2c-48d9-b898-c1d8b2c946e6
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ClusterRegDeleteValue, ClusterRegDeleteValue function [Failover Cluster], _wolf_clusterregdeletevalue, clusapi/ClusterRegDeleteValue, mscs.clusterregdeletevalue
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
 - ClusterRegDeleteValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegDeleteValue function


## -description


Removes a 
    named value from a <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle to a currently open key.


### -param lpszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to be removed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



Do not call <b>ClusterRegDeleteValue</b> from the 
     following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367196(v=VS.85).aspx">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa371770(v=VS.85).aspx">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa371773(v=VS.85).aspx">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a>
</li>
</ul>
<b>ClusterRegDeleteValue</b> can be safely called 
     from any other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369004(v=VS.85).aspx">ClusterRegOpenKey</a>
 

 

