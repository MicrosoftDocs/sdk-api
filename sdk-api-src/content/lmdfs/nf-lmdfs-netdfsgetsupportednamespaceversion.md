---
UID: NF:lmdfs.NetDfsGetSupportedNamespaceVersion
title: NetDfsGetSupportedNamespaceVersion function
author: windows-sdk-content
description: Determines the supported metadata version number.
old-location: dfs\netdfsgetsupportednamespaceversion.htm
old-project: Dfs
ms.assetid: 32ccf4a7-9d07-45e1-93db-29eddee01680
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: NetDfsGetSupportedNamespaceVersion, NetDfsGetSupportedNamespaceVersion function [Distributed File System], dfs.netdfsgetsupportednamespaceversion, fs.netdfsgetsupportednamespaceversion, lmdfs/NetDfsGetSupportedNamespaceVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DFS_TARGET_PRIORITY_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetDfsGetSupportedNamespaceVersion
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetDfsGetSupportedNamespaceVersion function


## -description


Determines the supported metadata version number.


## -parameters




### -param Origin [in]

A <a href="https://msdn.microsoft.com/b260e132-41fd-460b-87e6-c6e0490dc8b4">DFS_NAMESPACE_VERSION_ORIGIN</a> enumeration value that specifies the origin of the DFS namespace version.


### -param pName [in]

A string that specifies the server name or domain name. If the value of the <i>Origin</i> parameter is <b>DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN</b>, this string must be an AD DS domain name. Otherwise, it must be a server name. This parameter is required and cannot be <b>NULL</b>.


### -param ppVersionInfo [out]

A pointer to a <a href="https://msdn.microsoft.com/ee75c500-70c6-4dce-9d38-36cacd695746">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a> structure that receives the DFS metadata version number.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



This function is useful in determining an appropriate version number to pass to the <a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a> function.

The version number of the DFS metadata that can be used for a new DFS namespace depends on the following:

<ul>
<li>For domain-based DFS namespaces, the version supported by the DFS metadata schema that is being used in the AD DS domain.</li>
<li>The version supported by the server that is to host the DFS root target.</li>
</ul>
Thus, the maximum DFS metadata version number that can be used for a new DFS namespace is the minimum of the version supported by the AD DS domain and the version supported by the server. This maximum can be determined by calling the <b>NetDfsGetSupportedNamespaceVersion</b> function with the <i>pName</i> parameter set to the name of the server that is to host the new DFS root target and the <i>Origin</i> parameter set to <b>DFS_NAMESPACE_VERSION_ORIGIN_COMBINED</b>.




## -see-also




<a href="https://msdn.microsoft.com/b260e132-41fd-460b-87e6-c6e0490dc8b4">DFS_NAMESPACE_VERSION_ORIGIN</a>



<a href="https://msdn.microsoft.com/ee75c500-70c6-4dce-9d38-36cacd695746">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

