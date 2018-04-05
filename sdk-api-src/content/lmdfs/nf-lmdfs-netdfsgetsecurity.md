---
UID: NF:lmdfs.NetDfsGetSecurity
title: NetDfsGetSecurity function
author: windows-driver-content
description: Retrieves the security descriptor for the root object of the specified DFS namespace.
old-location: dfs\netdfsgetsecurity.htm
old-project: Dfs
ms.assetid: a6db7c82-c2ec-464a-8c05-2360622880b4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: NetDfsGetSecurity, NetDfsGetSecurity function [Distributed File System], dfs.netdfsgetsecurity, fs.netdfsgetsecurity, lmdfs/NetDfsGetSecurity, netmgmt.netdfsgetsecurity
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DFS_TARGET_PRIORITY_CLASS, DFS_TARGET_PRIORITY_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetDfsGetSecurity
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetDfsGetSecurity function


## -description


Retrieves the security descriptor for the root object of the specified DFS namespace.


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


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to retrieve from the root object.


### -param ppSecurityDescriptor [out]

Pointer to a list of <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structures that contain the security items requested in the <i>SecurityInformation</i> parameter.

<div class="alert"><b>Note</b>  This buffer must be freed by calling the <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.</div>
<div> </div>

### -param lpcbSecurityDescriptor [out]

The size of the buffer that <i>ppSecurityDescriptor</i> points to, in bytes.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



For domain-based DFS namespaces, the security descriptor is retrieved from the "CN=<i>DomDfsName</i>,CN=DFS-Configuration,CN=System,DC=<i>domain</i>" object in Active Directory from the primary domain controller (PDC) of the domain that hosts the DFS namespace, where <i>DomDfsName</i> is the name of the domain-based DFS namespace and &lt;domain&gt; is the distinguished name of the Active Directory domain that hosts the namespace.

For stand-alone roots, the security descriptor is retrieved from the object specified by the <b>HKLM</b>\<b>Software</b>\<b>Microsoft</b>\<b>Dfs</b>\<b>Standalone</b>\<b>&lt;root-name&gt;</b> registry entry.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/7ee81f67-face-498f-b5bd-ca2636408012">NetDfsSetSecurity</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

