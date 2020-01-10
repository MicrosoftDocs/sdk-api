---
UID: NF:lmdfs.NetDfsGetStdContainerSecurity
title: NetDfsGetStdContainerSecurity function (lmdfs.h)
description: Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.
old-location: dfs\netdfsgetstdcontainersecurity.htm
tech.root: Dfs
ms.assetid: 63ad610e-c66f-4fad-b3b6-2ee15e90a723
ms.date: 12/05/2018
ms.keywords: NetDfsGetStdContainerSecurity, NetDfsGetStdContainerSecurity function [Distributed File System], dfs.netdfsgetstdcontainersecurity, fs.netdfsgetstdcontainersecurity, lmdfs/NetDfsGetStdContainerSecurity, netmgmt.netdfsgetstdcontainersecurity
f1_keywords:
- lmdfs/NetDfsGetStdContainerSecurity
dev_langs:
- c++
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
- NetDfsGetStdContainerSecurity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetDfsGetStdContainerSecurity function


## -description


Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.


## -parameters




### -param MachineName [in]

Pointer to a string that specifies the name of the server that hosts the stand-alone DFS namespace.


### -param SecurityInformation [in]


<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to retrieve.


### -param ppSecurityDescriptor [out]

Pointer to a list of <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structures that contain the security items requested in the <i>SecurityInformation</i> parameter.

<div class="alert"><b>Note</b>  This buffer must be freed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.</div>
<div> </div>

### -param lpcbSecurityDescriptor [out]

The size of the buffer that <i>ppSecurityDescriptor</i> points to, in bytes.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



The security descriptor is retrieved from the object specified by the <b>HKLM</b>\<b>Software</b>\<b>Microsoft</b>\<b>Dfs</b>\<b>Standalone</b> key in the registry of the server specified in the <i>MachineName</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>
 

 

