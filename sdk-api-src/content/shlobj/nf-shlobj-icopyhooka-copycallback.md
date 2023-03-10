---
UID: NF:shlobj.ICopyHookA.CopyCallback
title: ICopyHookA::CopyCallback
description: Determines whether the Shell will be allowed to move, copy, delete, or rename a folder or printer object. (ANSI)
helpviewer_keywords: ["ICopyHookA::CopyCallback"]
tech.root: shell
ms.assetid: 50cba486-12b2-4ac7-8bf2-37b5784bb9fe
ms.date: 01/30/2019
ms.keywords: ICopyHookA::CopyCallback
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shlobj.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ICopyHookA::CopyCallback
 - shlobj/ICopyHookA::CopyCallback
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shlobj.h
api_name:
 - ICopyHookA::CopyCallback
---

## -description

Determines whether the Shell will be allowed to move, copy, delete, or rename a folder or printer object.

## -parameters

### -param hwnd

A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display. If **FOF_SILENT** is specified in *wFunc*, the method should ignore this parameter.

### -param wFunc

The operation to perform. This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.

### -param wFlags

The flags that control the operation. This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure. 
                        
For printer copy hooks, this value is one of the following values defined in Shellapi.h.

                 

| Value       | Description |
|-------------|------------|
|  **PO_DELETE**      | A printer is being deleted. *pszSrcFile* points to the full path to the specified printer.           |
|  **PO_RENAME**       | A printer is being renamed. The *pszSrcFile* parameter points to the printer's new name. The *pszDestFile* parameter points to the old name.           |
| **PO_PORTCHANGE**    | Not supported. Do not use.          |
| **PO_REN_PORT**    | Not supported. Do not use.           |

### -param pszSrcFile

A pointer to a string that contains the name of the source folder.

### -param dwSrcAttribs

The attributes of the source folder. This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_*) defined in the header files. See [File Attribute Constants](/windows/desktop/FileIO/file-attribute-constants).

### -param pszDestFile

A pointer to a string that contains the name of the destination folder.

### -param dwDestAttribs

The attributes of the destination folder. This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_*) defined in the header files. See [File Attribute Constants](/windows/desktop/FileIO/file-attribute-constants).

## -returns

Returns an integer value that indicates whether the Shell should perform the operation. One of the following:

| Value       | Description |
|-------------|------------|
| **IDYES**       | Allows the operation.           |
| **IDNO**        | Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).           |
| **IDCANCEL**    | Prevents the current operation and cancels any pending operations.           |

## -remarks

The Shell calls each copy hook handler registered for a folder or printer object until all the handlers have been called, or until one of them returns IDNO or IDCANCEL.

Copy hook handlers for folders are registered under the following key:

**HKEY_CLASSES_ROOT/Directory/Shellex/CopyHookHandlers/your_copyhook/{copyhook CLSID value}**

Copy hook handlers for printers are registered under the following key.

**HKEY_CLASSES_ROOT/Printers/Shellex/CopyHookHandlers/your_copyhook/{copyhook CLSID value}**
                
When this method is called, the Shell initializes the [ICopyHookA](nn-shlobj-icopyhooka.md) interface directly without using an [IShellExtInit](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.

## -see-also
