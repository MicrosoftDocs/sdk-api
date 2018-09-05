---
UID: NF:shobjidl.SHSetDefaultProperties
title: SHSetDefaultProperties function
author: windows-sdk-content
description: Applies the default set of properties on a Shell item.
old-location: shell\SHSetDefaultProperties.htm
old-project: shell
ms.assetid: c3ab80a3-c1f3-4223-9fe3-f7fe48c36460
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SHSetDefaultProperties, SHSetDefaultProperties function [Windows Shell], _shell_SHSetDefaultProperties, shell.SHSetDefaultProperties, shobjidl/SHSetDefaultProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHSetDefaultProperties
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# SHSetDefaultProperties function


## -description


Applies the default set of properties on a Shell item.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the item's parent window, which receives error notifications. This value can be <b>NULL</b>.


### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the item.


### -param dwFileOpFlags

Type: <b>DWORD</b>

Flags that customize the operation. See <a href="https://msdn.microsoft.com/1c2b9be8-d9b7-4ed4-a6da-e8166ddc35b3">IFileOperation::SetOperationFlags</a> for flag values.


### -param pfops [in, optional]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> object used to follow the progress of the operation. See <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a> for details. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The list of properties to set a default value comes from the <b>SetDefaultsFor</b> registry entry under the ProgID for the file association of the item. The list is prefixed by "<code>prop:</code>" and contains the canonical names of the properties to set the default value, for example, "<code>prop:System.Author;System.Document.DateCreated</code>". The possible properties for this list are <a href="https://msdn.microsoft.com/07a411c2-9e88-4d14-b9f7-e3a5d8d1630e">System.Author</a>, <a href="https://msdn.microsoft.com/00d8faa6-6b9c-4981-aeb1-17f8f14b1926">System.Document.DateCreated</a>, and <a href="https://msdn.microsoft.com/197fb739-7fe6-47e8-908f-54e75cb47ec4">System.Photo.DateTaken</a>. If the <b>SetDefaultsFor</b> entry does not exist on the ProgID, this function uses the default found on the <b>SetDefaultsFor</b> entry of <b>HKEY_CLASSES_ROOT</b>\<b>*</b>.



