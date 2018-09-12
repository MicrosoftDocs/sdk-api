---
UID: NF:resapi.ResUtilCreateDirectoryTree
title: ResUtilCreateDirectoryTree function
author: windows-sdk-content
description: Creates every directory specified in a path, skipping directories that already exist. The PRESUTIL_CREATE_DIRECTORY_TREE type defines a pointer to this function.
old-location: mscs\resutilcreatedirectorytree.htm
tech.root: mscs
ms.assetid: 5e1e689f-cc33-4cc7-9c6c-9799a6d6f70a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PRESUTIL_CREATE_DIRECTORY_TREE, PRESUTIL_CREATE_DIRECTORY_TREE function [Failover Cluster], ResUtilCreateDirectoryTree, ResUtilCreateDirectoryTree function [Failover Cluster], _wolf_resutilcreatedirectorytree, mscs.resutilcreatedirectorytree, resapi/PRESUTIL_CREATE_DIRECTORY_TREE, resapi/ResUtilCreateDirectoryTree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilCreateDirectoryTree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilCreateDirectoryTree function


## -description


Creates every directory specified in a path, skipping directories that already exist. The <b>PRESUTIL_CREATE_DIRECTORY_TREE</b> type defines a pointer to this function.


## -parameters




### -param pszPath [in]

Pointer to a null-terminated Unicode string specifying a path. The string can end with a trailing backslash.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



If the path only contains a drive specification (L"c:\\"),  <b>ResUtilCreateDirectoryTree</b> will return <b>ERROR_SUCCESS</b> but take no action.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// BEFORE
//   C:
//   |--Program Files
//      |-- MyApp
//          |--Data
ResUtilCreateDirectoryTree( L"C:\\Program Files\\MyApp\\Startup\\Parameters\\Users" );

ResUtilCreateDirectoryTree( L"C:\\Program Files\\MyApp\\Data\\Archive\\" );

ResUtilCreateDirectoryTree( L"C:\\Program Files\\MyApp\\Bin" );

// This call will return ERROR_SUCCESS even though all directories
// in the path already exist.
ResUtilCreateDirectoryTree( L"C:\\Program Files\\MyApp\\Bin" );

// AFTER
//   C:
//   |--Program Files
//      |--MyApp
//         |--Bin
//         |--Data
//         |  |--Archive
//         |--Startup
//            |--Parameters
//               |--Users
//
</pre>
</td>
</tr>
</table></span></div>


