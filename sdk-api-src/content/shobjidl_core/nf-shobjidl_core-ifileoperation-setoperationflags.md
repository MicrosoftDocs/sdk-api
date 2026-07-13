---
UID: NF:shobjidl_core.IFileOperation.SetOperationFlags
title: IFileOperation::SetOperationFlags (shobjidl_core.h)
description: Sets parameters for the current operation.
helpviewer_keywords: ["FOFX_ADDUNDORECORD","FOFX_COPYASDOWNLOAD","FOFX_DONTDISPLAYDESTPATH","FOFX_DONTDISPLAYLOCATIONS","FOFX_DONTDISPLAYSOURCEPATH","FOFX_EARLYFAILURE","FOFX_KEEPNEWERFILE","FOFX_MOVEACLSACROSSVOLUMES","FOFX_NOCOPYHOOKS","FOFX_NOMINIMIZEBOX","FOFX_NOSKIPJUNCTIONS","FOFX_PREFERHARDLINK","FOFX_PRESERVEFILEEXTENSIONS","FOFX_RECYCLEONDELETE","FOFX_REQUIREELEVATION","FOFX_SHOWELEVATIONPROMPT","FOF_ALLOWUNDO","FOF_FILESONLY","FOF_NOCONFIRMATION","FOF_NOCONFIRMMKDIR","FOF_NOCOPYSECURITYATTRIBS","FOF_NOERRORUI","FOF_NORECURSION","FOF_NO_CONNECTED_ELEMENTS","FOF_RENAMEONCOLLISION","FOF_SILENT","FOF_WANTNUKEWARNING","IFileOperation interface [Windows Shell]","SetOperationFlags method","IFileOperation.SetOperationFlags","IFileOperation::SetOperationFlags","SetOperationFlags","SetOperationFlags method [Windows Shell]","SetOperationFlags method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_SetOperationFlags","shell.IFileOperation_SetOperationFlags","shobjidl_core/IFileOperation::SetOperationFlags"]
old-location: shell\IFileOperation_SetOperationFlags.htm
tech.root: shell
ms.assetid: 1c2b9be8-d9b7-4ed4-a6da-e8166ddc35b3
ms.date: 12/05/2018
ms.keywords: FOFX_ADDUNDORECORD, FOFX_COPYASDOWNLOAD, FOFX_DONTDISPLAYDESTPATH, FOFX_DONTDISPLAYLOCATIONS, FOFX_DONTDISPLAYSOURCEPATH, FOFX_EARLYFAILURE, FOFX_KEEPNEWERFILE, FOFX_MOVEACLSACROSSVOLUMES, FOFX_NOCOPYHOOKS, FOFX_NOMINIMIZEBOX, FOFX_NOSKIPJUNCTIONS, FOFX_PREFERHARDLINK, FOFX_PRESERVEFILEEXTENSIONS, FOFX_RECYCLEONDELETE, FOFX_REQUIREELEVATION, FOFX_SHOWELEVATIONPROMPT, FOF_ALLOWUNDO, FOF_FILESONLY, FOF_NOCONFIRMATION, FOF_NOCONFIRMMKDIR, FOF_NOCOPYSECURITYATTRIBS, FOF_NOERRORUI, FOF_NORECURSION, FOF_NO_CONNECTED_ELEMENTS, FOF_RENAMEONCOLLISION, FOF_SILENT, FOF_WANTNUKEWARNING, IFileOperation interface [Windows Shell],SetOperationFlags method, IFileOperation.SetOperationFlags, IFileOperation::SetOperationFlags, SetOperationFlags, SetOperationFlags method [Windows Shell], SetOperationFlags method [Windows Shell],IFileOperation interface, _shell_IFileOperation_SetOperationFlags, shell.IFileOperation_SetOperationFlags, shobjidl_core/IFileOperation::SetOperationFlags
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileOperation::SetOperationFlags
 - shobjidl_core/IFileOperation::SetOperationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperation.SetOperationFlags
---

# IFileOperation::SetOperationFlags


## -description

Sets parameters for the current operation.

## -parameters

### -param dwOperationFlags [in]

Type: <b>DWORD</b>

Flags that control the file operation. This member can be a combination of the following flags. FOF flags are defined in Shellapi.h and FOFX flags are defined in Shobjidl.h.
    
                        

<div class="alert"><b>Note</b>  If this method is not called, the default value used by the operation is FOF_ALLOWUNDO | FOF_NOCONFIRMMKDIR.</div>
<div> </div>


#### FOF_ALLOWUNDO (0x0040)

Preserve undo information, if possible. 
                            
                                

Prior to Windows Vista, operations could be undone only from the same process that performed the original operation.

In Windows Vista and later systems, the scope of the undo is a user session. Any process running in the user session can undo another operation. The undo state is held in the Explorer.exe process, and as long as that process is running, it can coordinate the undo functions.

If the source file parameter does not contain fully qualified path and file names, this flag is ignored.



#### FOF_FILESONLY (0x0080)

Perform the operation only on files (not on folders) if a wildcard file name (*.*) is specified.



#### FOF_NOCONFIRMATION (0x0010)

Respond with <b>Yes to All</b> for any dialog box that is displayed.



#### FOF_NOCONFIRMMKDIR (0x0200)

Do not confirm the creation of a new folder if the operation requires one to be created.



#### FOF_NO_CONNECTED_ELEMENTS (0x2000)

Do not move connected items as a group. Only move the specified files.



#### FOF_NOCOPYSECURITYATTRIBS (0x0800)

Do not copy the security attributes of the item.



#### FOF_NOERRORUI (0x0400)

Do not display a message to the user if an error occurs. If this flag is set without FOFX_EARLYFAILURE, any error is treated as if the user had chosen <b>Ignore</b> or <b>Continue</b> in a dialog box. It halts the current action, sets a flag to indicate that an action was aborted, and proceeds with the rest of the operation.



#### FOF_NORECURSION (0x1000)

Only operate in the local folder. Do not operate recursively into subdirectories.



#### FOF_RENAMEONCOLLISION (0x0008)

Give the item being operated on a new name in a move, copy, or rename operation if an item with the target name already exists.



#### FOF_SILENT (0x0004)

Do not display a progress dialog box.



#### FOF_WANTNUKEWARNING (0x4000)

Send a warning if a file or folder is being destroyed during a delete operation rather than recycled. This flag partially overrides <b>FOF_NOCONFIRMATION</b>.



#### FOFX_ADDUNDORECORD (0x20000000)

<b>Introduced in Windows 8</b>. The file operation was user-invoked and should be placed on the undo stack. This flag is preferred to FOF_ALLOWUNDO.



#### FOFX_NOSKIPJUNCTIONS (0x00010000)

Walk into Shell namespace junctions. By default, junctions are not entered. For more information on junctions, see <a href="/previous-versions/windows/desktop/legacy/cc144096(v=vs.85)">Specifying a Namespace Extension's Location</a>.



#### FOFX_PREFERHARDLINK (0x00020000)

If possible, create a hard link rather than a new instance of the file in the destination.



#### FOFX_SHOWELEVATIONPROMPT (0x00040000)

If an operation requires elevated rights and the FOF_NOERRORUI flag is set to disable error UI, display a UAC UI prompt nonetheless.



#### FOFX_EARLYFAILURE (0x00100000)

If FOFX_EARLYFAILURE is set together with FOF_NOERRORUI, the entire set of operations is stopped upon encountering any error in any operation. This flag is valid only when FOF_NOERRORUI is set.



#### FOFX_PRESERVEFILEEXTENSIONS (0x00200000)

Rename collisions in such a way as to preserve file name extensions. This flag is valid only when FOF_RENAMEONCOLLISION is also set.



#### FOFX_KEEPNEWERFILE (0x00400000)

Keep the newer file or folder, based on the Date Modified property, if a collision occurs. This is done automatically with no prompt UI presented to the user.



#### FOFX_NOCOPYHOOKS (0x00800000)

Do not use copy hooks.



#### FOFX_NOMINIMIZEBOX (0x01000000)

Do not allow the progress dialog to be minimized.



#### FOFX_MOVEACLSACROSSVOLUMES (0x02000000)

Copy the security attributes of the source item to the destination item when performing a cross-volume move operation. Without this flag, the destination item receives the security attributes of its new folder.



#### FOFX_DONTDISPLAYSOURCEPATH (0x04000000)

Do not display the path of the source item in the progress dialog.



#### FOFX_DONTDISPLAYDESTPATH (0x08000000)

Do not display the path of the destination item in the progress dialog.



#### FOFX_RECYCLEONDELETE (0x00080000)

<b>Introduced in Windows 8</b>. When a file is deleted, send it to the Recycle Bin rather than permanently deleting it.



#### FOFX_REQUIREELEVATION (0x10000000)

<b>Introduced in Windows Vista SP1</b>. The user expects a requirement for rights elevation, so do not display a dialog box asking for a confirmation of the elevation.



#### FOFX_COPYASDOWNLOAD (0x40000000)

<b>Introduced in Windows 7</b>. Display a <b>Downloading</b> instead of <b>Copying</b> message in the progress dialog.



#### FOFX_DONTDISPLAYLOCATIONS (0x80000000)

<b>Introduced in Windows 7</b>. Do not display the location line in the progress dialog.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Set these flags before you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to define the parameters for whatever operations are being performed, such as copy, delete, or rename.