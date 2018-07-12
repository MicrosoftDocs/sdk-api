---
UID: NF:shobjidl_core.IShellLibrary.GetFolderType
title: IShellLibrary::GetFolderType
author: windows-sdk-content
description: Gets the library's folder type.
old-location: shell\IShellLibrary_GetFolderType.htm
old-project: shell
ms.assetid: 450ee4cc-5a09-4f14-832a-3982ec9de03b
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetFolderType, GetFolderType method [Windows Shell], GetFolderType method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetFolderType method, IShellLibrary.GetFolderType, IShellLibrary::GetFolderType, _shell_IShellLibrary_GetFolderType, shell.IShellLibrary_GetFolderType, shobjidl_core/IShellLibrary::GetFolderType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IShellLibrary.GetFolderType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLibrary::GetFolderType


## -description



         Gets the library's folder type.      
      


## -parameters




### -param pftid [out]

Type: <b><a href="https://msdn.microsoft.com/d147a05c-6a03-4f20-a7be-20825fcbeec2">FOLDERTYPEID</a>*</b>


            The  view template that is applied to a folder, usually based on its intended use and contents.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The folder type determines the default view template that is used by the folder. A view template specifies the columns and details that appear by default in the Windows Explorer view of the folder.


<a href="https://msdn.microsoft.com/d147a05c-6a03-4f20-a7be-20825fcbeec2">FOLDERTYPEID</a> values are GUID  values that are defined in shlguid.h.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>



<a href="https://msdn.microsoft.com/240550F0-B6AC-470e-8BF1-DB5A4068226B">folderType Element (Library Schema)</a>
 

 

