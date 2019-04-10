---
UID: NF:lmdfs.NetDfsSetSecurity
title: NetDfsSetSecurity function (lmdfs.h)
author: windows-sdk-content
description: Sets the security descriptor for the root object of the specified DFS namespace.
old-location: dfs\netdfssetsecurity.htm
tech.root: Dfs
ms.assetid: 7ee81f67-face-498f-b5bd-ca2636408012
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetDfsSetSecurity, NetDfsSetSecurity function [Distributed File System], dfs.netdfssetsecurity, fs.netdfssetsecurity, lmdfs/NetDfsSetSecurity, netmgmt.netdfssetsecurity
ms.topic: function
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
 - NetDfsSetSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetDfsSetSecurity function


## -description


Sets the security descriptor for the root object of the specified DFS namespace.


## -parameters




### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS namespace root.

The string can be in one of two forms. The first form is as follows:

\\<i>ServerName</i>\<i>DfsName</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace and <i>Dfsname</i> is the name of the DFS namespace.

The second form is as follows:

\\<i>DomainName</i>\<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace and <i>DomDfsName</i> is the name of the DFS namespace.


### -param SecurityInformation [in]


<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to set on the root object.


### -param pSecurityDescriptor [in]


<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that contains the security descriptor to set as specified in the <i>SecurityInformation</i> parameter.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



For domain-based DFS namespaces, the security descriptor is set on the  "CN=<i>DomDfsName</i>,CN=DFS-Configuration,CN=System,DC=<i>domain</i>" object in Active Directory at the primary domain controller (PDC) of the domain that hosts the DFS namespace, where &lt;<i>DomDfsName</i>&gt; is the name of the domain-based DFS namespace and &lt;domain&gt; is the distinguished name of the Active Directory domain that hosts the namespace.

For stand-alone roots, the security descriptor is set on the object specified by the <b>HKLM</b>\<b>Software</b>\<b>Microsoft</b>\<b>Dfs</b>\<b>Standalone</b>\<b>&lt;root-name&gt;</b> registry entry.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/a6db7c82-c2ec-464a-8c05-2360622880b4">NetDfsGetSecurity</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

