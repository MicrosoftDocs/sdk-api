---
UID: NF:shobjidl_core.IShellLibrary.Commit
title: IShellLibrary::Commit (shobjidl_core.h)
author: windows-sdk-content
description: Commits library updates to an existing Library Description file.
old-location: shell\IShellLibrary_Commit.htm
tech.root: shell
ms.assetid: a340964d-ea20-4a3b-be8b-f4f4dbf624ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Shell], Commit method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],Commit method, IShellLibrary.Commit, IShellLibrary::Commit, _shell_IShellLibrary_Commit, shell.IShellLibrary_Commit, shobjidl_core/IShellLibrary::Commit
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
 - IShellLibrary.Commit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLibrary::Commit


## -description


Commits library updates to an existing Library Description file.
      


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IShellLibrary::Commit</b>  can only be called to save library updates to an existing file.  A call to <b>IShellLibrary::Commit</b> 
            for a library that does not have a backing file will fail.
         
            To create and save a new file, call  <a href="https://msdn.microsoft.com/2a7de829-f0bc-4ace-aed4-83d0611ae292">IShellLibrary::Save</a> or <a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a>.
         

If the library is saved in the Libraries known folder (FOLDERID_Libraries), the folders in the library are automatically added to the search index.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/2a7de829-f0bc-4ace-aed4-83d0611ae292">IShellLibrary::Save</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

