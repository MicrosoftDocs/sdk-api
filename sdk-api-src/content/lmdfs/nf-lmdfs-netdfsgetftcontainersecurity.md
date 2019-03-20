---
UID: NF:lmdfs.NetDfsGetFtContainerSecurity
title: NetDfsGetFtContainerSecurity function (lmdfs.h)
author: windows-sdk-content
description: Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.
old-location: dfs\netdfsgetftcontainersecurity.htm
tech.root: Dfs
ms.assetid: 88e988db-1418-49d5-8cac-1ea6144474a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NetDfsGetFtContainerSecurity, NetDfsGetFtContainerSecurity function [Distributed File System], dfs.netdfsgetftcontainersecurity, fs.netdfsgetftcontainersecurity, lmdfs/NetDfsGetFtContainerSecurity, netmgmt.netdfsgetftcontainersecurity
ms.topic: function
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
---

# NetDfsGetFtContainerSecurity function


## -description


Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.


## -parameters




### -param DomainName [in]

Pointer to a string that specifies the Active Directory domain name.


### -param SecurityInformation [in]


<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to retrieve.


### -param ppSecurityDescriptor [out]

Pointer to a list <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structures that contain the security items requested in the <i>SecurityInformation</i> parameter.

<div class="alert"><b>Note</b>  This buffer must be freed by calling the <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.</div>
<div> </div>

### -param lpcbSecurityDescriptor [out]

The size of <i>ppSecurityDescriptor</i>, in bytes.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The security descriptor is retrieved from the "CN=DFS-Configuration,CN=System,DC=<i>domain</i>" object in Active Directory from the primary domain controller (PDC) of the domain specified in the <i>DomainName</i> parameter, where <i>domain</i> is the distinguished name of the domain specified in the <i>DomainName</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

