---
UID: NF:shobjidl_core.IFileSystemBindData.SetFindData
title: IFileSystemBindData::SetFindData
author: windows-driver-content
description: Stores file system information in a WIN32_FIND_DATA structure. This information is used by ParseDisplayName.
old-location: shell\IFileSystemBindData_SetFindData.htm
old-project: shell
ms.assetid: 8e2af85f-5eca-46e4-b193-bf25e2366fac
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IFileSystemBindData interface [Windows Shell],SetFindData method, IFileSystemBindData.SetFindData, IFileSystemBindData::SetFindData, SetFindData, SetFindData method [Windows Shell], SetFindData method [Windows Shell],IFileSystemBindData interface, _shell_ifilesystembinddata_setfinddata, shell.IFileSystemBindData_SetFindData, shobjidl_core/IFileSystemBindData::SetFindData
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
req.typenames: OVERLAPPED, *LPOVERLAPPED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileSystemBindData.SetFindData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IFileSystemBindData::SetFindData


## -description


Stores file system information in a <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure. This information is used by <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">ParseDisplayName</a>.


## -parameters




### -param pfd [in]

Type: <b>const <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure that specifies the data you want to store.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



After the client stores the file information, the instance of the object itself must be stored in a bind context by using the <a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">IBindCtx::RegisterObjectParam</a> method with the <i>pszKey</i> parameter set to <code>L"File System Bind Data"</code>.



