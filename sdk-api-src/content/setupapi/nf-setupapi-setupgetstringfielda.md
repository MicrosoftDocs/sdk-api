---
UID: NF:setupapi.SetupGetStringFieldA
title: SetupGetStringFieldA function (setupapi.h)
description: The SetupGetStringField function retrieves a string from the specified field of a line in an INF file. (ANSI)
helpviewer_keywords: ["SetupGetStringFieldA", "setupapi/SetupGetStringFieldA"]
old-location: setup\setupgetstringfield.htm
tech.root: setup
ms.assetid: fc735827-37ae-4d77-a0d4-4d31f0225d69
ms.date: 12/05/2018
ms.keywords: SetupGetStringField, SetupGetStringField function [Setup API], SetupGetStringFieldA, SetupGetStringFieldW, _setupapi_setupgetstringfield, setup.setupgetstringfield, setupapi/SetupGetStringField, setupapi/SetupGetStringFieldA, setupapi/SetupGetStringFieldW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetStringFieldW (Unicode) and SetupGetStringFieldA (ANSI)
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
 - SetupGetStringFieldA
 - setupapi/SetupGetStringFieldA
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
 - SetupGetStringField
 - SetupGetStringFieldA
 - SetupGetStringFieldW
req.apiset: ext-ms-win-setupapi-inf-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetupGetStringFieldA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetStringField</b> function retrieves a string from the specified field of a line in an INF file.

## -parameters

### -param Context [in]

Pointer to the context for a line in an INF file.

### -param FieldIndex [in]

The 1-based index of the field within the specified line from which the string should be retrieved. Use a <i>FieldIndex</i> of 0 to retrieve a string key, if present.

### -param ReturnBuffer [in, out]

Optional pointer to a  buffer that receives the <b>null</b>-terminated string. You should ensure the destination buffer is the same size or larger than the source buffer.  This parameter can be <b>NULL</b>. See the Remarks section.

### -param ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This includes the <b>null</b> terminator.

### -param RequiredSize [out]

Optional pointer to a variable that receives the required size  for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. If <i>ReturnBuffer</i> is specified and the actual size needed is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and does not store the string in the buffer. In this case, a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.  For the Unicode version of this function, the required size is in characters. This includes the <b>null</b> terminator.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size.



Note that the maximum length of any single string specified in an INF Strings section is 512 characters, including the terminating <b>NULL</b>. If the string length is greater than 512 it will be truncated and no error will be returned. The maximum length of any concatenated string created from one or more %strkey% tokens is 4096 characters.





> [!NOTE]
> The setupapi.h header defines SetupGetStringField as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetbinaryfield">SetupGetBinaryField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetintfield">SetupGetIntField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetmultiszfielda">SetupGetMultiSzField</a>
