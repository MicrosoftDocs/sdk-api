---
UID: NF:lmdfs.NetDfsSetFtContainerSecurity
title: NetDfsSetFtContainerSecurity function
author: windows-driver-content
description: Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.
old-location: dfs\netdfssetftcontainersecurity.htm
old-project: Dfs
ms.assetid: 84300e38-b263-4c38-bc31-5221621b89f1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: NetDfsSetFtContainerSecurity, NetDfsSetFtContainerSecurity function [Distributed File System], dfs.netdfssetftcontainersecurity, fs.netdfssetftcontainersecurity, lmdfs/NetDfsSetFtContainerSecurity, netmgmt.netdfssetftcontainersecurity
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
-	NetDfsSetFtContainerSecurity
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetDfsSetFtContainerSecurity function


## -description


Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.


## -parameters




### -param DomainName [in]

Pointer to a string that specifies the Active Directory domain name.


### -param SecurityInformation [in]


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> structure that contains bit flags that indicate the type of security information to set.


### -param pSecurityDescriptor [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure that contains the security attributes to set as specified in the <i>SecurityInformation</i> parameter.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The security descriptor is set on the "CN=DFS-Configuration,CN=System,DC=<i>domain</i>" object in Active Directory from the primary domain controller (PDC) of the domain specified in the <i>DomainName</i> parameter, where &lt;domain&gt; is the distinguished name of the domain specified in the <i>DomainName</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
    Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
    Overview</a>
 

 

