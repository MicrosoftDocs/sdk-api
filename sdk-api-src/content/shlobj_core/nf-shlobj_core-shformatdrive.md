---
UID: NF:shlobj_core.SHFormatDrive
title: SHFormatDrive function (shlobj_core.h)
description: SHFormatDrive may be altered or unavailable.
helpviewer_keywords: ["SHFMT_ID_DEFAULT","SHFMT_OPT_FULL","SHFMT_OPT_SYSONLY","SHFormatDrive","SHFormatDrive function [Windows Shell]","shell.SHFormatDrive","shell_SHFormatDrive","shlobj_core/SHFormatDrive"]
old-location: shell\SHFormatDrive.htm
tech.root: shell
ms.assetid: 4aa255fa-c407-47db-9b1f-d449e0a0e94f
ms.date: 12/05/2018
ms.keywords: SHFMT_ID_DEFAULT, SHFMT_OPT_FULL, SHFMT_OPT_SYSONLY, SHFormatDrive, SHFormatDrive function [Windows Shell], shell.SHFormatDrive, shell_SHFormatDrive, shlobj_core/SHFormatDrive
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
 - SHFormatDrive
 - shlobj_core/SHFormatDrive
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
 - SHFormatDrive
---

# SHFormatDrive function


## -description

<p class="CCE_Message">[<b>SHFormatDrive</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Opens the Shell's <b>Format</b> dialog box.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the dialog box. The <b>Format</b> dialog box must have a parent window; therefore, this parameter cannot be <b>NULL</b>.

### -param drive

Type: <b>UINT</b>

The drive to format. The value of this parameter represents a letter drive starting at 0 for the A: drive. For example, a value of 2 stands for the C: drive.

### -param fmtID

Type: <b>UINT</b>

The ID of the physical format. Only the following flag is currently defined.



#### SHFMT_ID_DEFAULT (0xFFFF)

The default format ID.

### -param options

Type: <b>UINT</b>

This value must be 0 or one of the following values that alter the default format options in the dialog box. This value is regarded as a bitfield and should be treated accordingly.



#### SHFMT_OPT_FULL (0x0001)

0x001. If this flag is set, then the <b>Quick Format</b> option is selected.

This function is included in Shlobj.h only in Windows XP with SP1 and later.

<b>Windows XP:  </b>Prior to Windows XP with SP1, this function is accessible through Shell32.lib.



#### SHFMT_OPT_SYSONLY (0x0002)

0x002. Selects the <b>Create an MS-DOS startup disk</b> option, creating a system boot disk.

## -returns

Type: <b>DWORD</b>

Returns the format ID of the last successful format or one of the following values. The LOWORD of this value can be passed on subsequent calls as the <i>fmtID</i> parameter to repeat the last format.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SHFMT_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during the last format. This does not indicate that the drive is unformattable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SHFMT_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The last format was canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SHFMT_NOFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The drive cannot be formatted.

</td>
</tr>
</table>

## -remarks

The format is controlled by the dialog box interface. That is, the user must click the <b>OK</b> button to actually begin the format—the format cannot be started programmatically.


#### Examples

This call to <b>SHFormatDrive</b> brings up the Shell's Format dialog box for a disk in drive A, with the default formatting options selected.


``` syntax
SHFormatDrive(hMainWnd, 0, SHFMT_ID_DEFAULT, 0);
```


