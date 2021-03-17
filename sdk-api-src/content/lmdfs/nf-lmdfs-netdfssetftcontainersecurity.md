---
UID: NF:lmdfs.NetDfsSetFtContainerSecurity
title: NetDfsSetFtContainerSecurity function (lmdfs.h)
description: Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.
helpviewer_keywords: ["NetDfsSetFtContainerSecurity","NetDfsSetFtContainerSecurity function [Distributed File System]","dfs.netdfssetftcontainersecurity","fs.netdfssetftcontainersecurity","lmdfs/NetDfsSetFtContainerSecurity","netmgmt.netdfssetftcontainersecurity"]
old-location: dfs\netdfssetftcontainersecurity.htm
tech.root: Dfs
ms.assetid: 84300e38-b263-4c38-bc31-5221621b89f1
ms.date: 12/05/2018
ms.keywords: NetDfsSetFtContainerSecurity, NetDfsSetFtContainerSecurity function [Distributed File System], dfs.netdfssetftcontainersecurity, fs.netdfssetftcontainersecurity, lmdfs/NetDfsSetFtContainerSecurity, netmgmt.netdfssetftcontainersecurity
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetDfsSetFtContainerSecurity
 - lmdfs/NetDfsSetFtContainerSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsSetFtContainerSecurity
---

# NetDfsSetFtContainerSecurity function


## -description

Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.

## -parameters

### -param DomainName [in]

Pointer to a string that specifies the Active Directory domain name.

### -param SecurityInformation [in]

<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to set.

### -param pSecurityDescriptor [in]

Pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the security attributes to set as specified in the <i>SecurityInformation</i> parameter.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The security descriptor is set on the "CN=DFS-Configuration,CN=System,DC=<i>domain</i>" object in Active Directory from the primary domain controller (PDC) of the domain specified in the <i>DomainName</i> parameter, where &lt;domain&gt; is the distinguished name of the domain specified in the <i>DomainName</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>