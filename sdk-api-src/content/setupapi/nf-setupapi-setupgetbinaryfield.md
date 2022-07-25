---
UID: NF:setupapi.SetupGetBinaryField
title: SetupGetBinaryField function (setupapi.h)
description: The SetupGetBinaryField function retrieves binary data from a line in an INF file section, from the specified field to the end of the line.
helpviewer_keywords: ["SetupGetBinaryField","SetupGetBinaryField function [Setup API]","_setupapi_setupgetbinaryfield","setup.setupgetbinaryfield","setupapi/SetupGetBinaryField"]
old-location: setup\setupgetbinaryfield.htm
tech.root: setup
ms.assetid: 6dfd4c8b-0197-4c6d-a780-084b428805b2
ms.date: 12/05/2018
ms.keywords: SetupGetBinaryField, SetupGetBinaryField function [Setup API], _setupapi_setupgetbinaryfield, setup.setupgetbinaryfield, setupapi/SetupGetBinaryField
req.header: setupapi.h
req.include-header: 
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupGetBinaryField
 - setupapi/SetupGetBinaryField
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
 - SetupGetBinaryField
---

# SetupGetBinaryField function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetBinaryField</b> function retrieves binary data from a line in an INF file section, from the specified field to the end of the line.

## -parameters

### -param Context [in]

INF context for the line.

### -param FieldIndex [in]

The 1-based index of the starting field within the specified line from which the binary data should be retrieved. The binary data is built from each field, starting at this point to the end of the line. Each field corresponds to 1 byte and is in hexadecimal notation. A <i>FieldIndex</i> of zero is not valid with this function.

### -param ReturnBuffer [in, out]

Optional pointer to a buffer that receives the binary data. You should ensure the destination buffer is the same size or larger than the source buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section.

### -param ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This number includes the <b>null</b> terminator.

### -param RequiredSize [in, out]

Optional pointer to a variable that receives the required size for the buffer pointed to <i>ReturnBuffer</i>, in characters. This number includes the <b>null</b> terminator. If the size needed is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_DATA if a field that 
<b>SetupGetBinaryField</b> retrieves is not a valid hexadecimal number in the range 0-FF.

## -remarks

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


To better understand how this function works, consider the following line from an INF file.


``` syntax
X=34,FF,00,13
```

If 
<b>SetupGetBinaryField</b> was called on the preceding line, the binary values 34, FF, 00, and 13 would be put into the buffer specified by <i>ReturnBuffer</i>.

For the Unicode version of this function, the buffer sizes <i>ReturnBufferSize</i> and <i>RequiredSize</i> are specified in number of characters. This number includes the <b>null</b> terminator. For the ANSI version of this function, the sizes are specified in number of bytes.

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Thus, you can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetintfield">SetupGetIntField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetmultiszfielda">SetupGetMultiSzField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetstringfielda">SetupGetStringField</a>
