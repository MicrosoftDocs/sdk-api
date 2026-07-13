---
UID: NF:setupapi.SetupBackupErrorW
title: SetupBackupErrorW function (setupapi.h)
description: The SetupBackupError function generates a dialog box that informs the user of a backup error. (Unicode)
helpviewer_keywords: ["SetupBackupError", "SetupBackupError function [Setup API]", "SetupBackupErrorW", "_setupapi_setupbackuperror", "setup.setupbackuperror", "setupapi/SetupBackupError", "setupapi/SetupBackupErrorW"]
old-location: setup\setupbackuperror.htm
tech.root: setup
ms.assetid: 4c2a8a63-29e7-4750-9239-6693754dff58
ms.date: 12/05/2018
ms.keywords: SetupBackupError, SetupBackupError function [Setup API], SetupBackupErrorA, SetupBackupErrorW, _setupapi_setupbackuperror, setup.setupbackuperror, setupapi/SetupBackupError, setupapi/SetupBackupErrorA, setupapi/SetupBackupErrorW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupBackupErrorW (Unicode) and SetupBackupErrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupBackupErrorW
 - setupapi/SetupBackupErrorW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupBackupError
 - SetupBackupErrorA
 - SetupBackupErrorW
---

# SetupBackupErrorW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupBackupError</b> function generates a dialog box that informs the user of a backup error.

## -parameters

### -param hwndParent [in]

Handle to the parent window for this dialog box.

### -param DialogTitle [in]

Optional pointer to a <b>null</b>-terminated string specifying the error dialog box title. If this parameter is <b>NULL</b>, the default title of "Backup Error" (localized) is used.

### -param SourceFile [in]

Pointer to a <b>null</b>-terminated string specifying the full path of the source file that is being backed up.

### -param TargetFile [in]

Optional pointer to a <b>null</b>-terminated string specifying the full path of the backup name of the file. This parameter can be <b>NULL</b>.

### -param Win32ErrorCode [out]

If an error occurs, this member is the <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. If no error has occurred, it is  NO_ERROR.

### -param Style [in]

Flags that control display formatting and behavior of the dialog box. This parameter can be one of the following flags. 







#### IDF_NOBEEP

Prevent the dialog box from beeping to get the user's attention when it first appears.



#### IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.


##### - Style.IDF_NOBEEP

Prevent the dialog box from beeping to get the user's attention when it first appears.


##### - Style.IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.

## -returns

This function returns one of the following values.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcopyerrora">SetupCopyError</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdeleteerrora">SetupDeleteError</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuppromptfordiska">SetupPromptForDisk</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuprenameerrora">SetupRenameError</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupBackupError as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
