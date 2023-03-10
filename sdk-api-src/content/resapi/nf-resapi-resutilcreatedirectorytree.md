---
UID: NF:resapi.ResUtilCreateDirectoryTree
title: ResUtilCreateDirectoryTree function (resapi.h)
description: Creates every directory specified in a path, skipping directories that already exist. The PRESUTIL_CREATE_DIRECTORY_TREE type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_CREATE_DIRECTORY_TREE","PRESUTIL_CREATE_DIRECTORY_TREE function [Failover Cluster]","ResUtilCreateDirectoryTree","ResUtilCreateDirectoryTree function [Failover Cluster]","_wolf_resutilcreatedirectorytree","mscs.resutilcreatedirectorytree","resapi/PRESUTIL_CREATE_DIRECTORY_TREE","resapi/ResUtilCreateDirectoryTree"]
old-location: mscs\resutilcreatedirectorytree.htm
tech.root: MsCS
ms.assetid: 5e1e689f-cc33-4cc7-9c6c-9799a6d6f70a
ms.date: 12/05/2018
ms.keywords: PRESUTIL_CREATE_DIRECTORY_TREE, PRESUTIL_CREATE_DIRECTORY_TREE function [Failover Cluster], ResUtilCreateDirectoryTree, ResUtilCreateDirectoryTree function [Failover Cluster], _wolf_resutilcreatedirectorytree, mscs.resutilcreatedirectorytree, resapi/PRESUTIL_CREATE_DIRECTORY_TREE, resapi/ResUtilCreateDirectoryTree
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilCreateDirectoryTree
 - resapi/ResUtilCreateDirectoryTree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilCreateDirectoryTree
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
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

If the path only contains a drive specification (L"c:\\"),  <b>ResUtilCreateDirectoryTree</b> will return <b>ERROR_SUCCESS</b> but take no action.


#### Examples


```cpp
// BEFORE
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

```