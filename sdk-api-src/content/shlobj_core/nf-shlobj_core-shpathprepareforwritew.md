---
UID: NF:shlobj_core.SHPathPrepareForWriteW
title: SHPathPrepareForWriteW function (shlobj_core.h)
description: Checks to see if the path exists. (Unicode)
helpviewer_keywords: ["SHPPFW_ASKDIRCREATE", "SHPPFW_DEFAULT", "SHPPFW_DIRCREATE", "SHPPFW_IGNOREFILENAME", "SHPPFW_MEDIACHECKONLY", "SHPPFW_NONE", "SHPPFW_NOWRITECHECK", "SHPathPrepareForWrite", "SHPathPrepareForWrite function [Windows Shell]", "SHPathPrepareForWriteW", "_shell_shpathprepareforwrite", "shell.SHPathPrepareForWrite", "shlobj_core/SHPathPrepareForWrite", "shlobj_core/SHPathPrepareForWriteW"]
old-location: shell\SHPathPrepareForWrite.htm
tech.root: shell
ms.assetid: 1b65e34f-2c31-421b-9d27-ed263dfb372b
ms.date: 12/05/2018
ms.keywords: SHPPFW_ASKDIRCREATE, SHPPFW_DEFAULT, SHPPFW_DIRCREATE, SHPPFW_IGNOREFILENAME, SHPPFW_MEDIACHECKONLY, SHPPFW_NONE, SHPPFW_NOWRITECHECK, SHPathPrepareForWrite, SHPathPrepareForWrite function [Windows Shell], SHPathPrepareForWriteA, SHPathPrepareForWriteW, _shell_shpathprepareforwrite, shell.SHPathPrepareForWrite, shlobj_core/SHPathPrepareForWrite, shlobj_core/SHPathPrepareForWriteA, shlobj_core/SHPathPrepareForWriteW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHPathPrepareForWriteW (Unicode) and SHPathPrepareForWriteA (ANSI)
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
 - SHPathPrepareForWriteW
 - shlobj_core/SHPathPrepareForWriteW
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
 - SHPathPrepareForWrite
 - SHPathPrepareForWriteA
 - SHPathPrepareForWriteW
---

# SHPathPrepareForWriteW function


## -description

Checks to see if the path exists. This includes remounting mapped network drives, prompting for ejectable media to be reinserted, creating the paths, prompting for the media to be formatted, and providing the appropriate user interfaces, if necessary. Read/write permissions for the medium are not checked.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to a window that specifies the parent window to be used for any user interface windows that must be created. If set to <b>NULL</b>, user interface windows are not created.

### -param punkEnableModless [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that specifies the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a> object that implements the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-enablemodeless">EnableModeless</a> method.

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that specifies the path to be verified as valid for writing. This can be a UNC or file drive path.

### -param dwFlags

Type: <b>DWORD</b>

Flags that determine behavior options. This parameter can be a combination of the following values.



#### SHPPFW_NONE

Do not create new directories.



#### SHPPFW_DEFAULT

Default. Do not prompt the user if a directory needs to be created. This is identical to <b>SHPPFW_DIRCREATE</b>. Do not pass with <b>SHPPFW_ASKDIRCREATE</b>.



#### SHPPFW_DIRCREATE

Create directories without prompting the user. Do not pass with <b>SHPPFW_ASKDIRCREATE</b>.



#### SHPPFW_ASKDIRCREATE

Prompt the user before creating directories. Do not pass with <b>SHPPFW_DIRCREATE</b>.



#### SHPPFW_IGNOREFILENAME

Last item in <i>pszPath</i> is a file name, so ignore. For example, if <i>pszPath</i>="C:\MyDir\MyFile.doc", only use "C:\MyDir". If <i>pszPath</i>="C:\MyFirDir\MySecDir", only use "C:\MyFirDir".



#### SHPPFW_NOWRITECHECK

Not currently implemented.



#### SHPPFW_MEDIACHECKONLY

<b>Windows XP or later.</b> Suppresses the "not accessible" error message box, which displays when a failure other than a user cancellation occurs, and <i>hwnd</i> is not <b>NULL</b>.


##### - dwFlags.SHPPFW_ASKDIRCREATE

Prompt the user before creating directories. Do not pass with <b>SHPPFW_DIRCREATE</b>.


##### - dwFlags.SHPPFW_DEFAULT

Default. Do not prompt the user if a directory needs to be created. This is identical to <b>SHPPFW_DIRCREATE</b>. Do not pass with <b>SHPPFW_ASKDIRCREATE</b>.


##### - dwFlags.SHPPFW_DIRCREATE

Create directories without prompting the user. Do not pass with <b>SHPPFW_ASKDIRCREATE</b>.


##### - dwFlags.SHPPFW_IGNOREFILENAME

Last item in <i>pszPath</i> is a file name, so ignore. For example, if <i>pszPath</i>="C:\MyDir\MyFile.doc", only use "C:\MyDir". If <i>pszPath</i>="C:\MyFirDir\MySecDir", only use "C:\MyFirDir".


##### - dwFlags.SHPPFW_MEDIACHECKONLY

<b>Windows XP or later.</b> Suppresses the "not accessible" error message box, which displays when a failure other than a user cancellation occurs, and <i>hwnd</i> is not <b>NULL</b>.


##### - dwFlags.SHPPFW_NONE

Do not create new directories.


##### - dwFlags.SHPPFW_NOWRITECHECK

Not currently implemented.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the path is available, or an error code otherwise. Note that a return value of S_OK does not mean that the medium is writable; it simply means that the path is available.

## -remarks

The primary use of this function is for a program to check a path before using it and display the necessary user interface to prompt the user. For example, if the disk in drive A: were missing, a window that prompts the user to insert the disk would appear.




> [!NOTE]
> The shlobj_core.h header defines SHPathPrepareForWrite as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
