---
UID: NF:lmdfs.NetDfsSetStdContainerSecurity
title: NetDfsSetStdContainerSecurity function (lmdfs.h)
author: windows-sdk-content
description: Sets the security descriptor for the container object of the specified stand-alone DFS namespace.
old-location: dfs\netdfssetstdcontainersecurity.htm
tech.root: Dfs
ms.assetid: bc408a12-5106-45a0-bbed-0468d51708bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetDfsSetStdContainerSecurity, NetDfsSetStdContainerSecurity function [Distributed File System], dfs.netdfssetstdcontainersecurity, fs.netdfssetstdcontainersecurity, lmdfs/NetDfsSetStdContainerSecurity, netmgmt.netdfssetstdcontainersecurity
ms.topic: function
f1_keywords: ["lmdfs/NetDfsSetStdContainerSecurity"]
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsSetStdContainerSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetDfsSetStdContainerSecurity function


## -description


Sets the security descriptor for the container object of the specified stand-alone DFS namespace.


## -parameters




### -param MachineName [in]

The name of the stand-alone DFS root's host machine. Pointer to a string that specifies the name of the server that hosts the stand-alone DFS namespace.


### -param SecurityInformation [in]


<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to set on the root object.


### -param pSecurityDescriptor [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the security attributes to set as specified in the <i>SecurityInformation</i> parameter.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



The security descriptor is set for the object specified by the <b>HKLM</b>\<b>Software</b>\<b>Microsoft</b>\<b>Dfs</b>\<b>Standalone</b> key in the registry of the server specified in the <i>MachineName</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>
 

 

