---
UID: NF:shobjidl_core.IShellLibrary.SetFolderType
title: IShellLibrary::SetFolderType (shobjidl_core.h)
author: windows-sdk-content
description: Sets the library's folder type.
old-location: shell\IShellLibrary_SetFolderType.htm
tech.root: shell
ms.assetid: e3e3f356-6ffd-46b9-b8a5-1b0c9df01abe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],SetFolderType method, IShellLibrary.SetFolderType, IShellLibrary::SetFolderType, SetFolderType, SetFolderType method [Windows Shell], SetFolderType method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SetFolderType, shell.IShellLibrary_SetFolderType, shobjidl_core/IShellLibrary::SetFolderType
ms.topic: method
f1_keywords: ["shobjidl_core/IShellLibrary.SetFolderType"]
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IShellLibrary.SetFolderType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellLibrary::SetFolderType


## -description


Sets the library's folder type.
      


## -parameters




### -param ftid [in]

Type: <b>REFFOLDERTYPEID</b>

The <b>GUID</b> or <a href="https://docs.microsoft.com/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a> that represents  the  view template that is applied to a folder, usually based on its intended use and contents.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The folder type determines the default view template that is used by the folder. A view template specifies the  columns and details that appear by default in Windows Explorer by default view of the folder.  <a href="https://docs.microsoft.com/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a> values are GUID  values that are defined in shlguid.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd798386(v=vs.85)">folderType Element (Library Schema)</a>
 

 

