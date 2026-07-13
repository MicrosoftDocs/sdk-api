---
UID: NF:setupapi.SetupCopyErrorA
title: SetupCopyErrorA function (setupapi.h)
description: The SetupCopyError function generates a dialog box to notify a user of a copy file error. (ANSI)
helpviewer_keywords: ["SetupCopyErrorA", "setupapi/SetupCopyErrorA"]
old-location: setup\setupcopyerror.htm
tech.root: setup
ms.assetid: bda8ffef-f1a7-474c-9ec6-f76c2f006d51
ms.date: 12/05/2018
ms.keywords: SetupCopyError, SetupCopyError function [Setup API], SetupCopyErrorA, SetupCopyErrorW, _setupapi_setupcopyerror, setup.setupcopyerror, setupapi/SetupCopyError, setupapi/SetupCopyErrorA, setupapi/SetupCopyErrorW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupCopyErrorW (Unicode) and SetupCopyErrorA (ANSI)
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
 - SetupCopyErrorA
 - setupapi/SetupCopyErrorA
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
 - SetupCopyError
 - SetupCopyErrorA
 - SetupCopyErrorW
---

# SetupCopyErrorA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCopyError</b> function generates a dialog box to notify a user of a copy file error.

## -parameters

### -param hwndParent [in]

The handle to the parent window for this dialog box.

### -param DialogTitle [in]

An optional pointer to a <b>null</b>-terminated string that specifies the dialog box title. 

This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the default title of "Copy Error" (localized to the system language) is used.

### -param DiskName [in]

An optional pointer to a <b>null</b>-terminated string that specifies the name of the disk to insert.  

This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the default name "(Unknown)" (localized to the system language) is used.

### -param PathToSource [in]

A pointer to the path component of the source file where an operation fails, for example, F:\x86. 

Use a <b>null</b>-terminated string.

### -param SourceFile [in]

A pointer to a <b>null</b>-terminated string that specifies the filename part of the file where an operation fails. 

Use a <b>null</b>-terminated string. This filename is displayed if the user clicks on the <b>Details</b> or <b>Browse</b> buttons. The <b>SetupCopyError</b> function looks for the file that uses its compressed form names. Therefore, you can pass cmd.exe and not worry that the file actually exists as cmd.ex_ on the source media.

### -param TargetPathFile [in]

An optional pointer to a <b>null</b>-terminated string that specifies the full path of the target file for rename and copy operations. 

Use a <b>null</b>-terminated string.  This parameter can be <b>NULL</b>. If TargetPathFile is not specified, "(Unknown)" (localized to the system language) is used.

### -param Win32ErrorCode [out]

If an error occurs, this member is the <a href="/windows/desktop/Debug/system-error-codes">System Error Code</a>. 

If an error does not occur, it is  NO_ERROR.

### -param Style [in]

The flags that control display formatting and behavior of a dialog box. 

This parameter can be one of the following flags.





#### IDF_NOBROWSE

Do not display the browse option.



#### IDF_NOSKIP

Do not display the skip file option.



#### IDF_NODETAILS

Do not display the details option. 

If this flag is set, the <i>TargetPathFile</i> and <i>Win32ErrorCode</i> parameters can be omitted.



#### IDF_NOCOMPRESSED

Do not check for compressed versions of the source file.



#### IDF_OEMDISK

The operation source is a disk that a hardware manufacturer provides.



#### IDF_NOBEEP

Prevents the dialog box from beeping to get the user's attention when it first appears.



#### IDF_NOFOREGROUND

Prevents the dialog box from becoming the foreground window.



#### IDF_WARNIFSKIP

Warns the user that skipping a file can affect the installation.

### -param PathBuffer [in, out]

An optional pointer to a variable in which this function returns the path (not including the filename) of the location that a user specifies in the dialog box. You should use a null-terminated string. 

The <b>null</b>-terminated string should not exceed the size of the destination buffer. To avoid insufficient buffer errors, <i>PathBuffer</i> should be at least MAX_PATH.
For more information, see the Remarks section of this topic.

### -param PathBufferSize [in]

 The size of the buffer that  <i>PathBuffer</i> points to, in characters. 

The buffer size should be at least MAX_PATH characters, including the <b>null</b> terminator.

### -param PathRequiredSize [in, out]

An optional pointer to a variable in which this function returns the required buffer size, in characters, including the <b>null</b> terminator.

## -returns

The function returns one of the following values.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>PathBuffer</i> of <b>NULL</b> and a <i>PathBufferSize</i> of 0 (zero), the function puts the buffer size that is needed to hold the specified data into the variable pointed to by <i>PathRequiredSize</i>. 

If the function succeeds, the return value is NO_ERROR. Otherwise, the return value is one of the specified values.

To avoid insufficient buffer errors, <i>ReturnBuffer</i> should be at least MAX_PATH.





> [!NOTE]
> The setupapi.h header defines SetupCopyError as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdeleteerrora">SetupDeleteError</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuppromptfordiska">SetupPromptForDisk</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuprenameerrora">SetupRenameError</a>
