---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NetDfsRemoveRootTarget function


## -description


Removes a DFS root target from a domain-based  DFS namespace. If the root target is the last root target 
    in the DFS namespace, this function removes the DFS namespace. This function can also be used to remove a 
    stand-alone DFS namespace.


## -parameters




### -param pDfsPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS namespace.

For a stand-alone DFS namespace, this string should be in the following form:

\\<i>ServerName</i>\<i>DfsName</i>

where <i>ServerName</i> is the name of the server that hosts the DFS root target and 
       <i>DfsName</i> is the name of the DFS namespace.

For a domain-based DFS namespace, this string should be in the following form:

\\<i>DomainName</i>\<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace and <i>DomDfsName</i> is the name of the DFS namespace.


### -param pTargetPath [in, optional]

Pointer to a null-terminated Unicode string that specifies the UNC path of a DFS root target for the DFS 
       namespace that is specified in the <i>pDfsPath</i> parameter.

For a stand-alone DFS namespace, this parameter must be <b>NULL</b>. For a domain-based 
       DFS namespace, the string should be in the following form:

\\<i>ServerName</i>\<i>RootShare</i>

where <i>ServerName</i> is the name of the server that hosts the DFS root target and 
       <i>RootShare</i> is the name of the folder on the server.


### -param Flags [in]

A flag that specifies the type of removal operation. For a stand-alone DFS namespace, this parameter must 
      be zero. For a domain-based DFS namespace, it can be zero or the following value. If it is zero, this indicates 
      a normal removal operation.



#### DFS_FORCE_REMOVE (0x80000000)

If this flag is specified for a domain-based DFS namespace, the root target is removed even if it is not 
        accessible.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller must have Administrator privileges on the DFS server.

The following list shows which parameter values you should specify, according to the desired result.

<table>
<tr>
<th><i>pDfsPath</i> parameter</th>
<th><i>pTargetPath</i> parameter</th>
<th>Result</th>
</tr>
<tr>
<td>\\<i>DomainName</i>\<i>DomDfsName</i></td>
<td>\\<i>ServerName</i>\<i>RootShare</i></td>
<td>Delete a Windows 2000 mode or Windows Server 2008 mode domain-based DFS root target. If the 
       target is the last root target for the DFS namespace, the function also deletes the DFS namespace.</td>
</tr>
<tr>
<td>\\<i>ServerName</i>\<i>DfsName</i></td>
<td><b>NULL</b></td>
<td>Delete a stand-alone DFS namespace.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>
 

 

