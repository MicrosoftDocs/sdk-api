---
UID: NF:setupapi.SetupRenameErrorW
title: SetupRenameErrorW function (setupapi.h)
description: The RenameError function generates a dialog box that informs the user of a file renaming error.helpviewer_keywords: ["SetupRenameError","SetupRenameError function [Setup API]","SetupRenameErrorA","SetupRenameErrorW","_setupapi_setuprenameerror","setup.setuprenameerror","setupapi/SetupRenameError","setupapi/SetupRenameErrorA","setupapi/SetupRenameErrorW"]
old-location: setup\setuprenameerror.htm
tech.root: SetupApi
ms.assetid: 43371fa0-d7b4-42e0-a94d-d307a7210618
ms.date: 12/05/2018
ms.keywords: SetupRenameError, SetupRenameError function [Setup API], SetupRenameErrorA, SetupRenameErrorW, _setupapi_setuprenameerror, setup.setuprenameerror, setupapi/SetupRenameError, setupapi/SetupRenameErrorA, setupapi/SetupRenameErrorW
f1_keywords:
- setupapi/SetupRenameError
dev_langs:
- c++
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRenameErrorW (Unicode) and SetupRenameErrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Setupapi.dll
api_name:
- SetupRenameError
- SetupRenameErrorA
- SetupRenameErrorW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupRenameErrorW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>RenameError</b> function generates a dialog box that informs the user of a file renaming error.


## -parameters




### -param hwndParent [in]

Handle to the parent window for this dialog box.


### -param DialogTitle [in]

Pointer to a <b>null</b>-terminated string that specifies the error dialog box title. This parameter may be <b>NULL</b>. If this parameter is <b>NULL</b>, the default title of "Rename Error" (localized) is used.


### -param SourceFile [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the source file on which the operation failed.


### -param TargetFile [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the target file on which the operation failed.


### -param Win32ErrorCode [in]

The <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> encountered during the file operation. 


### -param Style [in]

Specifies display formatting and behavior of the dialog box. This parameter can be one of the following flags. 







#### IDF_NOBEEP

Prevent the dialog box from beeping when it first appears.



#### IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.


##### - Style.IDF_NOBEEP

Prevent the dialog box from beeping when it first appears.


##### - Style.IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.


## -returns



This function returns one of the following values.

To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupcopyerrora">SetupCopyError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdeleteerrora">SetupDeleteError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setuppromptfordiska">SetupPromptForDisk</a>
 

 

