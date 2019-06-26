---
UID: NF:lmdfs.NetDfsGetFtContainerSecurity
title: NetDfsGetFtContainerSecurity function (lmdfs.h)
author: windows-sdk-content
description: Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.
old-location: dfs\netdfsgetftcontainersecurity.htm
tech.root: Dfs
ms.assetid: 88e988db-1418-49d5-8cac-1ea6144474a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetDfsGetFtContainerSecurity, NetDfsGetFtContainerSecurity function [Distributed File System], dfs.netdfsgetftcontainersecurity, fs.netdfsgetftcontainersecurity, lmdfs/NetDfsGetFtContainerSecurity, netmgmt.netdfsgetftcontainersecurity
ms.topic: function
f1_keywords: 
 - "lmdfs/NetDfsGetFtContainerSecurity"
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
 - NetDfsGetFtContainerSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetDfsGetFtContainerSecurity function


## -description


Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.


## -parameters




### -param DomainName [in]

Pointer to a string that specifies the Active Directory domain name.


### -param SecurityInformation [in]


<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to retrieve.


### -param ppSecurityDescriptor [out]

Pointer to a list <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> structures that contain the security items requested in the <i>SecurityInformation</i> parameter.

<div class="alert"><b>Note</b>  This buffer must be freed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.</div>
<div> </div>

### -param lpcbSecurityDescriptor [out]

The size of <i>ppSecurityDescriptor</i>, in bytes.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



The security descriptor is retrieved from the "CN=DFS-Configuration,CN=System,DC=<i>domain</i>" object in Active Directory from the primary domain controller (PDC) of the domain specified in the <i>DomainName</i> parameter, where <i>domain</i> is the distinguished name of the domain specified in the <i>DomainName</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>
 

 

