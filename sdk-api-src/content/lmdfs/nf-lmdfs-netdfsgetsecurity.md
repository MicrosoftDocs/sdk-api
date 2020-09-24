---
UID: NF:lmdfs.NetDfsGetSecurity
title: NetDfsGetSecurity function (lmdfs.h)
description: Retrieves the security descriptor for the root object of the specified DFS namespace.
helpviewer_keywords: ["NetDfsGetSecurity","NetDfsGetSecurity function [Distributed File System]","dfs.netdfsgetsecurity","fs.netdfsgetsecurity","lmdfs/NetDfsGetSecurity","netmgmt.netdfsgetsecurity"]
old-location: dfs\netdfsgetsecurity.htm
tech.root: Dfs
ms.assetid: a6db7c82-c2ec-464a-8c05-2360622880b4
ms.date: 12/05/2018
ms.keywords: NetDfsGetSecurity, NetDfsGetSecurity function [Distributed File System], dfs.netdfsgetsecurity, fs.netdfsgetsecurity, lmdfs/NetDfsGetSecurity, netmgmt.netdfsgetsecurity
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
 - NetDfsGetSecurity
 - lmdfs/NetDfsGetSecurity
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
 - NetDfsGetSecurity
---

# NetDfsGetSecurity function


## -description

Retrieves the security descriptor for the root object of the specified DFS namespace.

## -parameters

### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS namespace root.

The string can be in one of two forms. The first form is as follows:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace and <i>Dfsname</i> is the name of the DFS namespace.

The second form is as follows:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace and <i>DomDfsName</i> is the name of the DFS namespace.

### -param SecurityInformation [in]

<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to retrieve from the root object.

### -param ppSecurityDescriptor [out]

Pointer to a list of <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structures that contain the security items requested in the <i>SecurityInformation</i> parameter.

<div class="alert"><b>Note</b>  This buffer must be freed by calling the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.</div>
<div> </div>

### -param lpcbSecurityDescriptor [out]

The size of the buffer that <i>ppSecurityDescriptor</i> points to, in bytes.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

For domain-based DFS namespaces, the security descriptor is retrieved from the "CN=<i>DomDfsName</i>,CN=DFS-Configuration,CN=System,DC=<i>domain</i>" object in Active Directory from the primary domain controller (PDC) of the domain that hosts the DFS namespace, where <i>DomDfsName</i> is the name of the domain-based DFS namespace and &lt;domain&gt; is the distinguished name of the Active Directory domain that hosts the namespace.

For stand-alone roots, the security descriptor is retrieved from the object specified by the <b>HKLM</b>&#92;<b>Software</b>&#92;<b>Microsoft</b>&#92;<b>Dfs</b>&#92;<b>Standalone</b>&#92;<b>&lt;root-name&gt;</b> registry entry.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity">NetDfsSetSecurity</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>