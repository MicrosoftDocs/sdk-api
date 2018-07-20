---
UID: NF:shobjidl_core.IFileSystemBindData2.GetFileID
title: IFileSystemBindData2::GetFileID
author: windows-sdk-content
description: Gets the unique file identifier for the current file.
old-location: shell\IFileSystemBindData2_GetFileID.htm
old-project: shell
ms.assetid: 77052ae5-d663-4bf8-967a-29bd5dc85706
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetFileID, GetFileID method [Windows Shell], GetFileID method [Windows Shell],IFileSystemBindData2 interface, IFileSystemBindData2 interface [Windows Shell],GetFileID method, IFileSystemBindData2.GetFileID, IFileSystemBindData2::GetFileID, _shell_IFileSystemBindData2_GetFileID, shell.IFileSystemBindData2_GetFileID, shobjidl_core/IFileSystemBindData2::GetFileID
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileSystemBindData2.GetFileID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileSystemBindData2::GetFileID


## -description


Gets the unique file identifier for the current file.


## -parameters




### -param pliFileID [out]

Type: <b>LARGE_INTEGER*</b>

When this method returns successfully, receives a pointer to the unique file identifier for the current file. <i>pliFileID</i> is a pointer to a value that is a concatenation of the values <i>nFileIndexHigh</i> and <i>nFileIndexlow</i>, noted in structure <a href="https://msdn.microsoft.com/a6fc5cf0-d3b0-4a76-af8b-6a13ab32157d">_by_handle_file_information</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



