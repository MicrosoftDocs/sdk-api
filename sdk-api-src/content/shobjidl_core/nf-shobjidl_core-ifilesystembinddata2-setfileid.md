---
UID: NF:shobjidl_core.IFileSystemBindData2.SetFileID
title: IFileSystemBindData2::SetFileID
author: windows-sdk-content
description: Sets the unique file identifier for the current file.
old-location: shell\IFileSystemBindData2_SetFileID.htm
tech.root: shell
ms.assetid: d3da2a22-cd45-4f3f-afcc-183a20f60f15
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileSystemBindData2 interface [Windows Shell],SetFileID method, IFileSystemBindData2.SetFileID, IFileSystemBindData2::SetFileID, SetFileID, SetFileID method [Windows Shell], SetFileID method [Windows Shell],IFileSystemBindData2 interface, _shell_IFileSystemBindData2_SetFileID, shell.IFileSystemBindData2_SetFileID, shobjidl_core/IFileSystemBindData2::SetFileID
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IFileSystemBindData2.SetFileID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemBindData2::SetFileID


## -description


Sets the unique file identifier for the current file.


## -parameters




### -param liFileID [in]

Type: <b>LARGE_INTEGER</b>

A unique file identifier for the current file.  <i>liFileID</i> is a value that is a concatenation of the values <i>nFileIndexHigh</i> and <i>nFileIndexlow</i>, noted in structure <a href="https://msdn.microsoft.com/a6fc5cf0-d3b0-4a76-af8b-6a13ab32157d">_by_handle_file_information</a>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



