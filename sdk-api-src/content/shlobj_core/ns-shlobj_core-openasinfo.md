---
UID: NS:shlobj_core._openasinfo
title: OPENASINFO (shlobj_core.h)
description: Stores information for the SHOpenWithDialog function.
helpviewer_keywords: ["*POPENASINFO","OAIF_ALLOW_REGISTRATION","OAIF_EXEC","OAIF_FILE_IS_URI","OAIF_FORCE_REGISTRATION","OAIF_HIDE_REGISTRATION","OAIF_REGISTER_EXT","OAIF_URL_PROTOCOL","OPENASINFO","OPENASINFO structure [Windows Shell]","_openasinfo","_shell_OPENASINFO","shell.OPENASINFO","shlobj_core/OPENASINFO"]
old-location: shell\OPENASINFO.htm
tech.root: shell
ms.assetid: 5486c4d3-c6c5-459d-aa7f-426971184876
ms.date: 12/05/2018
ms.keywords: '*POPENASINFO, OAIF_ALLOW_REGISTRATION, OAIF_EXEC, OAIF_FILE_IS_URI, OAIF_FORCE_REGISTRATION, OAIF_HIDE_REGISTRATION, OAIF_REGISTER_EXT, OAIF_URL_PROTOCOL, OPENASINFO, OPENASINFO structure [Windows Shell], _openasinfo, _shell_OPENASINFO, shell.OPENASINFO, shlobj_core/OPENASINFO'
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPENASINFO, *POPENASINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _openasinfo
 - shlobj_core/_openasinfo
 - POPENASINFO
 - shlobj_core/POPENASINFO
 - OPENASINFO
 - shlobj_core/OPENASINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - OPENASINFO
---

# OPENASINFO structure


## -description

Stores information for the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog">SHOpenWithDialog</a> function.

## -struct-fields

### -field pcszFile

Type: <b>LPCWSTR</b>

A pointer to the file name.

### -field pcszClass

Type: <b>LPCWSTR</b>

A pointer to the file type description. Set this parameter to <b>NULL</b> to use the file name extension of <b>pcszFile</b>.

### -field oaifInFlags

Type: <b>OPEN_AS_INFO_FLAGS</b>

The characteristics of the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog">SHOpenWithDialog</a> dialog box. One or more of the following values.



#### OAIF_ALLOW_REGISTRATION (0x00000001)

Enable the "always use this program" checkbox. If not passed, it will be disabled.



#### OAIF_REGISTER_EXT (0x00000002)

Do the registration after the user hits the <b>OK</b> button.



#### OAIF_EXEC (0x00000004)

Execute file after registering.



#### OAIF_FORCE_REGISTRATION (0x00000008)

Force the <b>Always use this program</b> checkbox to be checked. Typically, you won't use the OAIF_ALLOW_REGISTRATION flag when you pass this value.



#### OAIF_HIDE_REGISTRATION (0x00000020)

<b>Introduced in Windows Vista</b>. Hide the <b>Always use this program</b> checkbox. If this flag is specified, the OAIF_ALLOW_REGISTRATION and OAIF_FORCE_REGISTRATION flags will be ignored.



#### OAIF_URL_PROTOCOL (0x00000040)

<b>Introduced in Windows Vista</b>. The value for the extension that is passed is actually a protocol, so the <b>Open With</b> dialog box should show applications that are registered as capable of handling that protocol.



#### OAIF_FILE_IS_URI (0x00000080)

<b>Introduced in Windows 8</b>. The location pointed to by the <i>pcszFile</i> parameter is given as a URI.

## -remarks

Starting in Windows 10, the <b>OAIF_ALLOW_REGISTRATION</b>, <b>OAIF_FORCE_REGISTRATION</b>, and <b>OAIF_HIDE_REGISTRATION</b> flags will be ignored by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog">SHOpenWithDialog</a>. The <b>Open With</b> dialog box can no longer be used to change the default program used to open a file extension. You can only use <b>SHOpenWithDialog</b> to open a single file.