---
UID: NF:setupapi.SetupQueryInfVersionInformationA
title: SetupQueryInfVersionInformationA function (setupapi.h)
description: The SetupQueryInfVersionInformation function returns INF file version information from an SP_INF_INFORMATION structure to a buffer. (ANSI)
helpviewer_keywords: ["SetupQueryInfVersionInformationA", "setupapi/SetupQueryInfVersionInformationA"]
old-location: setup\setupqueryinfversioninformation.htm
tech.root: setup
ms.assetid: 58768b91-a0c7-4791-8667-2890b742798c
ms.date: 12/05/2018
ms.keywords: SetupQueryInfVersionInformation, SetupQueryInfVersionInformation function [Setup API], SetupQueryInfVersionInformationA, SetupQueryInfVersionInformationW, _setupapi_setupqueryinfversioninformation, setup.setupqueryinfversioninformation, setupapi/SetupQueryInfVersionInformation, setupapi/SetupQueryInfVersionInformationA, setupapi/SetupQueryInfVersionInformationW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueryInfVersionInformationW (Unicode) and SetupQueryInfVersionInformationA (ANSI)
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
 - SetupQueryInfVersionInformationA
 - setupapi/SetupQueryInfVersionInformationA
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
 - SetupQueryInfVersionInformation
 - SetupQueryInfVersionInformationA
 - SetupQueryInfVersionInformationW
---

# SetupQueryInfVersionInformationA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueryInfVersionInformation</b> function returns INF file version information from an 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_inf_information">SP_INF_INFORMATION</a> structure to a buffer.

## -parameters

### -param InfInformation [in]

Pointer to an 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_inf_information">SP_INF_INFORMATION</a> structure previously returned from a call to the 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfinformationa">SetupGetInfInformation</a> function.

### -param InfIndex [in]

Index of the constituent INF file to retrieve version information from. This index can be in the range [0, <i>InfInformation.InfCount</i>). Meaning that the values zero through, but not including, <i>InfInformation.InfCount</i> are valid.

### -param Key [in]

Optional pointer to a <b>null</b>-terminated string containing the key name whose associated string is to be retrieved. If this parameter is <b>NULL</b>, all resource keys are copied to the supplied buffer. Each string is <b>null</b>-terminated, with an extra <b>null</b> at the end of the list.

### -param ReturnBuffer [in, out]

If not <b>NULL</b>, <i>ReturnBuffer</i> points to a call-supplied character buffer in which this function returns the INF file style. You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section. This parameter can be <b>NULL</b>.

### -param ReturnBufferSize [in]

Size of the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This number includes the <b>null</b> terminator.

### -param RequiredSize [in, out]

If not <b>NULL</b>, pointer to a variable that receives the size required for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This number includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is specified and the actual size is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and a call to 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If 
<b>SetupQueryInfVersionInformation</b> is called on a legacy INF file , then version information is generated from the legacy INF file in the following manner:

<ol>
<li>The OptionType key in the <b>Identification</b> section of the legacy file  is returned as the Class key value.</li>
<li>The FileType key in the <b>Signature</b> section of the legacy INF file becomes the Signature key value.</li>
<li>If the value of the FileType key of the legacy INF file is MICROSOFT_FILE, then the Provider key value is set to "Microsoft".</li>
</ol>
The following table summarizes how the information is translated before it is passed into the 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_inf_information">SP_INF_INFORMATION</a> structure.

<table>
<tr>
<th>Legacy file information</th>
<th> Windows INF information</th>
</tr>
<tr>
<td>

``` syntax
[Identification]
OptionType = Mouse
```

</td>
<td>

``` syntax
[Version]
Class=Mouse
```

</td>
</tr>
<tr>
<td>

``` syntax
[Signature]
FileType = MICROSOFT_FILE
```

</td>
<td>

``` syntax
Signature=MICROSOFT_FILE
```

</td>
</tr>
<tr>
<td>(if the FileType is MICROSOFT_FILE)</td>
<td>

``` syntax
Provider="Microsoft"
```

</td>
</tr>
</table>
 





> [!NOTE]
> The setupapi.h header defines SetupQueryInfVersionInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfinformationa">SetupGetInfInformation</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueryinffileinformationa">SetupQueryInfFileInformation</a>
