---
UID: NF:setupapi.SetupDeleteErrorW
title: SetupDeleteErrorW function (setupapi.h)
description: The SetupDeleteError function generates a dialog box that informs the user of a delete error. (Unicode)
helpviewer_keywords: ["SetupDeleteError", "SetupDeleteError function [Setup API]", "SetupDeleteErrorW", "_setupapi_setupdeleteerror", "setup.setupdeleteerror", "setupapi/SetupDeleteError", "setupapi/SetupDeleteErrorW"]
old-location: setup\setupdeleteerror.htm
tech.root: setup
ms.assetid: 200e1926-7ebd-4373-803d-1c054db5df8d
ms.date: 12/05/2018
ms.keywords: SetupDeleteError, SetupDeleteError function [Setup API], SetupDeleteErrorA, SetupDeleteErrorW, _setupapi_setupdeleteerror, setup.setupdeleteerror, setupapi/SetupDeleteError, setupapi/SetupDeleteErrorA, setupapi/SetupDeleteErrorW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDeleteErrorW (Unicode) and SetupDeleteErrorA (ANSI)
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
 - SetupDeleteErrorW
 - setupapi/SetupDeleteErrorW
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
 - SetupDeleteError
 - SetupDeleteErrorA
 - SetupDeleteErrorW
---

# SetupDeleteErrorW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupDeleteError</b> function generates a dialog box that informs the user of a delete error.

## -parameters

### -param hwndParent [in]

Handle to the parent window for this dialog box.

### -param DialogTitle [in]

Optional pointer to a <b>null</b>-terminated string specifying the error dialog box title. If this parameter is <b>NULL</b>, the default title of "Delete Error" (localized) is used.

### -param File [in]

Pointer to a <b>null</b>-terminated string specifying the full path of the file on which the delete operation failed.

### -param Win32ErrorCode [out]

The <a href="/windows/desktop/Debug/system-error-codes">system error code</a> encountered during the file operation.

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



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuppromptfordiska">SetupPromptForDisk</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuprenameerrora">SetupRenameError</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDeleteError as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
