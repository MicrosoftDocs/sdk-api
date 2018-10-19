---
UID: NF:shobjidl_core.IFileSystemBindData.GetFindData
title: IFileSystemBindData::GetFindData
author: windows-sdk-content
description: Gets the file system information stored in the WIN32_FIND_DATA structure.
old-location: shell\IFileSystemBindData_GetFindData.htm
tech.root: shell
ms.assetid: 75161b45-42b9-4d64-ae13-583d07920a0b
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetFindData, GetFindData method [Windows Shell], GetFindData method [Windows Shell],IFileSystemBindData interface, IFileSystemBindData interface [Windows Shell],GetFindData method, IFileSystemBindData.GetFindData, IFileSystemBindData::GetFindData, _shell_ifilesystembinddata_getfinddata, shell.IFileSystemBindData_GetFindData, shobjidl_core/IFileSystemBindData::GetFindData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileSystemBindData.GetFindData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemBindData::GetFindData


## -description


Gets the file system information stored in the <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure.



## -parameters




### -param pfd [out]

Type: <b><a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure that receives the data.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK.




## -remarks



This method provides bind context information to <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a>. The client accesses the object by calling <a href="https://msdn.microsoft.com/8f423495-7a34-4901-968e-1fe204680d8a">IBindCtx::GetObjectParam</a> with the <i>pszKey</i> parameter set to the string "File System Bind Data".
      



