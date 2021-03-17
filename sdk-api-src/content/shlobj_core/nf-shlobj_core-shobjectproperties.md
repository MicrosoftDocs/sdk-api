---
UID: NF:shlobj_core.SHObjectProperties
title: SHObjectProperties function (shlobj_core.h)
description: SHObjectProperties may be altered or unavailable.
helpviewer_keywords: ["SHOP_FILEPATH","SHOP_PRINTERNAME","SHOP_VOLUMEGUID","SHObjectProperties","SHObjectProperties function [Windows Shell]","_win32_SHObjectProperties","shell.SHObjectProperties","shlobj_core/SHObjectProperties"]
old-location: shell\SHObjectProperties.htm
tech.root: shell
ms.assetid: 7517c461-955b-446e-85d7-a707c9bd183a
ms.date: 12/05/2018
ms.keywords: SHOP_FILEPATH, SHOP_PRINTERNAME, SHOP_VOLUMEGUID, SHObjectProperties, SHObjectProperties function [Windows Shell], _win32_SHObjectProperties, shell.SHObjectProperties, shlobj_core/SHObjectProperties
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHObjectProperties
 - shlobj_core/SHObjectProperties
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
 - SHObjectProperties
---

# SHObjectProperties function


## -description

<p class="CCE_Message">[<b>SHObjectProperties</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Invokes the <b>Properties</b> context menu command on a Shell object.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the dialog box. This value can be <b>NULL</b>.

### -param shopObjectType [in]

Type: <b>DWORD</b>

A flag value that specifies the type of object.



#### SHOP_PRINTERNAME

<i>pszObjectName</i> contains the friendly name of a printer.



#### SHOP_FILEPATH

<i>pszObjectName</i> contains a fully qualified file name.



#### SHOP_VOLUMEGUID

<i>pszObjectName</i> contains either (a) a volume name of the form \\?\Volume{GUID}\, where {GUID} is a globally unique identifier (for example, "\\?\Volume\{2eca078d-5cbc-43d3-aff8-7e8511f60d0e}\)", or (b) a drive path (for example, "C:\").

### -param pszObjectName [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the object name. The contents of the string are determined by the flag set in <i>shopObjectType</i>.

### -param pszPropertyPage [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the name of the property sheet page to be opened initially. Set this parameter to <b>NULL</b> to specify the default page.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the command is successfully invoked; otherwise, <b>FALSE</b>.

