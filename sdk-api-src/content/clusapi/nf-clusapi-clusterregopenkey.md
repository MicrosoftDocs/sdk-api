---
UID: NF:clusapi.ClusterRegOpenKey
title: ClusterRegOpenKey function
author: windows-driver-content
description: Opens an existing cluster database key.
old-location: mscs\clusterregopenkey.htm
old-project: MsCS
ms.assetid: f2cf204e-d02d-40b9-86d7-0262b8cc4db1
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ClusterRegOpenKey, ClusterRegOpenKey function [Failover Cluster], _wolf_clusterregopenkey, clusapi/ClusterRegOpenKey, mscs.clusterregopenkey
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClusAPI.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
-	ClusterRegOpenKey
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegOpenKey function


## -description


Opens an existing  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key.


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
The <i>lpszSubKey</i> parameter can point to an empty string, causing  <a href="https://msdn.microsoft.com/a5e924bd-9336-45c8-b2c9-48291f8db774">ClusterRegCreateKey</a> to return a handle to the database key represented by <i>hKey</i>.


### -param samDesired [in]

Access mask that specifies the security access needed for the new key.


### -param phkResult [out]

Pointer to a handle to the opened or created key.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Callers should call  <a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a> to close the key handle opened by  <b>ClusterRegOpenKey</b> when they are done with it.




## -see-also




<a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a>



<a href="https://msdn.microsoft.com/a5e924bd-9336-45c8-b2c9-48291f8db774">ClusterRegCreateKey</a>
 

 

