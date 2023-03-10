---
UID: NF:shobjidl.SHSetDefaultProperties
title: SHSetDefaultProperties function (shobjidl.h)
description: Applies the default set of properties on a Shell item.
helpviewer_keywords: ["SHSetDefaultProperties","SHSetDefaultProperties function [Windows Shell]","_shell_SHSetDefaultProperties","shell.SHSetDefaultProperties","shobjidl/SHSetDefaultProperties"]
old-location: shell\SHSetDefaultProperties.htm
tech.root: shell
ms.assetid: c3ab80a3-c1f3-4223-9fe3-f7fe48c36460
ms.date: 12/05/2018
ms.keywords: SHSetDefaultProperties, SHSetDefaultProperties function [Windows Shell], _shell_SHSetDefaultProperties, shell.SHSetDefaultProperties, shobjidl/SHSetDefaultProperties
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSetDefaultProperties
 - shobjidl/SHSetDefaultProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHSetDefaultProperties
---

# SHSetDefaultProperties function


## -description

Applies the default set of properties on a Shell item.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the item's parent window, which receives error notifications. This value can be <b>NULL</b>.

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the item.

### -param dwFileOpFlags

Type: <b>DWORD</b>

Flags that customize the operation. See <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setoperationflags">IFileOperation::SetOperationFlags</a> for flag values.

### -param pfops [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> object used to follow the progress of the operation. See <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a> for details. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The list of properties to set a default value comes from the <b>SetDefaultsFor</b> registry entry under the ProgID for the file association of the item. The list is prefixed by "<code>prop:</code>" and contains the canonical names of the properties to set the default value, for example, "<code>prop:System.Author;System.Document.DateCreated</code>". The possible properties for this list are <a href="/windows/desktop/properties/props-system-author">System.Author</a>, <a href="/windows/desktop/properties/props-system-document-datecreated">System.Document.DateCreated</a>, and <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a>. If the <b>SetDefaultsFor</b> entry does not exist on the ProgID, this function uses the default found on the <b>SetDefaultsFor</b> entry of <b>HKEY_CLASSES_ROOT</b>&#92;<b>*</b>.