---
UID: NF:shobjidl_core.IShellItemResources.GetAttributes
title: IShellItemResources::GetAttributes (shobjidl_core.h)
description: Gets resource attributes.
helpviewer_keywords: ["FILE_ATTRIBUTE_ARCHIVE","FILE_ATTRIBUTE_COMPRESSED","FILE_ATTRIBUTE_CONTENT_INDEXED","FILE_ATTRIBUTE_DIRECTORY","FILE_ATTRIBUTE_ENCRYPTED","FILE_ATTRIBUTE_HIDDEN","FILE_ATTRIBUTE_NORMAL","FILE_ATTRIBUTE_OFFLINE","FILE_ATTRIBUTE_READONLY","FILE_ATTRIBUTE_REPARSE_POINT","FILE_ATTRIBUTE_SPARSE_FILE","FILE_ATTRIBUTE_SYSTEM","FILE_ATTRIBUTE_TEMPORARY","FILE_ATTRIBUTE_VALID_FLAGS","FILE_ATTRIBUTE_VALID_SET_FLAGS","GetAttributes","GetAttributes method [Windows Shell]","GetAttributes method [Windows Shell]","IShellItemResources interface","IShellItemResources interface [Windows Shell]","GetAttributes method","IShellItemResources.GetAttributes","IShellItemResources::GetAttributes","_shell_IShellItemResources_GetAttributes","shell.IShellItemResources_GetAttributes","shobjidl_core/IShellItemResources::GetAttributes"]
old-location: shell\IShellItemResources_GetAttributes.htm
tech.root: shell
ms.assetid: 4669ec62-270a-4b75-b073-2f45f11b6f99
ms.date: 12/05/2018
ms.keywords: FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_COMPRESSED, FILE_ATTRIBUTE_CONTENT_INDEXED, FILE_ATTRIBUTE_DIRECTORY, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_REPARSE_POINT, FILE_ATTRIBUTE_SPARSE_FILE, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, FILE_ATTRIBUTE_VALID_FLAGS, FILE_ATTRIBUTE_VALID_SET_FLAGS, GetAttributes, GetAttributes method [Windows Shell], GetAttributes method [Windows Shell],IShellItemResources interface, IShellItemResources interface [Windows Shell],GetAttributes method, IShellItemResources.GetAttributes, IShellItemResources::GetAttributes, _shell_IShellItemResources_GetAttributes, shell.IShellItemResources_GetAttributes, shobjidl_core/IShellItemResources::GetAttributes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemResources::GetAttributes
 - shobjidl_core/IShellItemResources::GetAttributes
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
 - IShellItemResources.GetAttributes
---

# IShellItemResources::GetAttributes


## -description

Gets resource attributes.

## -parameters

### -param pdwAttributes [out]

Type: <b>DWORD*</b>

A pointer to resource attributes. The following are attribute values.



#### FILE_ATTRIBUTE_READONLY

Value is 0x00000001.



#### FILE_ATTRIBUTE_HIDDEN

Value is 0x00000002.



#### FILE_ATTRIBUTE_SYSTEM

Value is 0x00000004.



#### FILE_ATTRIBUTE_DIRECTORY

Value is 0x00000010.



#### FILE_ATTRIBUTE_ARCHIVE

Value is 0x00000020.



#### FILE_ATTRIBUTE_ENCRYPTED

Value is 0x00000040.



#### FILE_ATTRIBUTE_NORMAL

Value is 0x00000080.



#### FILE_ATTRIBUTE_TEMPORARY

Value is 0x00000100.



#### FILE_ATTRIBUTE_SPARSE_FILE

Value is 0x00000200.



#### FILE_ATTRIBUTE_REPARSE_POINT

Value is 0x00000400.



#### FILE_ATTRIBUTE_COMPRESSED

Value is 0x00000800.



#### FILE_ATTRIBUTE_OFFLINE

Value is 0x00001000.



#### FILE_ATTRIBUTE_CONTENT_INDEXED

Value is 0x00002000.



#### FILE_ATTRIBUTE_VALID_FLAGS

Value is 0x00001ff7.



#### FILE_ATTRIBUTE_VALID_SET_FLAGS

Value is 0x000011a7.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

