---
UID: NF:setupapi.SetupGetMultiSzFieldA
title: SetupGetMultiSzFieldA function (setupapi.h)
description: The SetupGetMultiSzField function retrieves multiple strings stored in a line of an INF file, from the specified field to the end of the line. (ANSI)
helpviewer_keywords: ["SetupGetMultiSzFieldA", "setupapi/SetupGetMultiSzFieldA"]
old-location: setup\setupgetmultiszfield.htm
tech.root: setup
ms.assetid: d884037c-a8d0-47a8-8b3f-70408866be05
ms.date: 12/05/2018
ms.keywords: SetupGetMultiSzField, SetupGetMultiSzField function [Setup API], SetupGetMultiSzFieldA, SetupGetMultiSzFieldW, _setupapi_setupgetmultiszfield, setup.setupgetmultiszfield, setupapi/SetupGetMultiSzField, setupapi/SetupGetMultiSzFieldA, setupapi/SetupGetMultiSzFieldW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetMultiSzFieldW (Unicode) and SetupGetMultiSzFieldA (ANSI)
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
 - SetupGetMultiSzFieldA
 - setupapi/SetupGetMultiSzFieldA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupGetMultiSzField
 - SetupGetMultiSzFieldA
 - SetupGetMultiSzFieldW
req.apiset: ext-ms-win-setupapi-inf-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetupGetMultiSzFieldA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetMultiSzField</b> function retrieves multiple strings stored in a line of an INF file, from the specified field to the end of the line.

## -parameters

### -param Context [in]

Pointer to the context for a line in an INF file.

### -param FieldIndex [in]

The 1-based index of the starting field within the specified line from which the strings should be retrieved. The string list is built from each field starting at this point to the end of the line. A <i>FieldIndex</i> of zero is not valid with this function.

### -param ReturnBuffer [in, out]

Optional pointer to a character buffer that receives the strings. Each string is <b>null</b>-terminated, with an extra <b>null</b> at the end of the string list. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section. This parameter can be <b>NULL</b>.

### -param ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This includes the <b>null</b> terminator.

### -param RequiredSize [in]

Optional pointer to a variable that receives the size required for the buffer pointed to by <i>ReturnBuffer</i>, in  characters. This includes the <b>null</b> terminator. If the size needed is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



<b>SetupGetMultiSzField</b> should not be used to iterate through string values on an INF line. Instead you should use <a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetstringfielda">SetupGetStringField</a>. <b>SetupGetMultiSzField</b> returns a value in the format of REG_MULTI_SZ. This is an array of <b>null</b>-terminated strings terminated by an extra <b>null</b> character. This format does not allow zero-length strings. If the list of strings contains any zero-length strings, <b>SetupGetMultiSzField</b> will return prematurely when it encounters the first blank string value. 






> [!NOTE]
> The setupapi.h header defines SetupGetMultiSzField as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetbinaryfield">SetupGetBinaryField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetintfield">SetupGetIntField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetstringfielda">SetupGetStringField</a>
