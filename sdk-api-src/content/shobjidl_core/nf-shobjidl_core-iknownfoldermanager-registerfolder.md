---
UID: NF:shobjidl_core.IKnownFolderManager.RegisterFolder
title: IKnownFolderManager::RegisterFolder
author: windows-sdk-content
description: Adds a new known folder to the registry. Used particularly by independent software vendors (ISVs) that are adding one of their own folders to the known folder system.
old-location: shell\IKnownFolderManager_RegisterFolder.htm
tech.root: shell
ms.assetid: 1b3d492f-26a3-4f04-ba01-768ebad39e1b
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IKnownFolderManager interface [Windows Shell],RegisterFolder method, IKnownFolderManager.RegisterFolder, IKnownFolderManager::RegisterFolder, RegisterFolder, RegisterFolder method [Windows Shell], RegisterFolder method [Windows Shell],IKnownFolderManager interface, _shell_IKnownFolderManager_RegisterFolder, shell.IKnownFolderManager_RegisterFolder, shobjidl_core/IKnownFolderManager::RegisterFolder
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolderManager.RegisterFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolderManager::RegisterFolder


## -description


Adds a new known folder to the registry. Used particularly by independent software vendors (ISVs) that are adding one of their own folders to the known folder system.


## -parameters




### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A <b>GUID</b> that represents the known folder.


### -param pKFD [in]

Type: <b>const KNOWNFOLDER_DEFINITION*</b>

A pointer to a valid <a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a> structure that provides the details of the new folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  This method updates <b>HKEY_LOCAL_MACHINE</b> and therefore needs to be run in the context of an administrator. Setup programs need administrator privileges to register or unregister a known folder.</div>
<div> </div>
<b>IKnownFolderManager::RegisterFolder</b> attempts to verify that the new <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> does not refer to a file system path already pointed to by an existing <b>KNOWNFOLDERID</b>. If the new <b>KNOWNFOLDERID</b> is found to do so, this method fails.

Multiple <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> values for the same file system path can cause several issues, such as conflicts in the Desktop.ini file that lead to confusion as to what language or properties to show for the folder. Multiple <b>KNOWNFOLDERID</b> values can also cause confusion as to the address bar path or what tasks to show for the folder in Windows Explorer.

You can suppress the display of the <b>Customize</b> page of your known folder's Properties window. To do so, set the following registry REG_DWORD value:

                <pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>FolderDescriptions</b>
                     <i>Folder GUID</i>
                        <b>PropertyBag</b>
                           <b>NoCustomize</b> = 0x00000001 (1)</pre>





## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/2c66f5e3-3479-414c-8888-0a888708dbe0">IKnownFolderManager::UnregisterFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

