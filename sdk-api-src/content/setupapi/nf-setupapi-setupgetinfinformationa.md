---
UID: NF:setupapi.SetupGetInfInformationA
title: SetupGetInfInformationA function (setupapi.h)
description: The SetUpGetInfInformation function returns the SP_INF_INFORMATION structure for the specified INF file to a buffer. (ANSI)
helpviewer_keywords: ["SetupGetInfInformationA", "setupapi/SetupGetInfInformationA"]
old-location: setup\setupgetinfinformation.htm
tech.root: setup
ms.assetid: 367eb374-1295-41f6-a1b3-cfc04e94b816
ms.date: 12/05/2018
ms.keywords: SetupGetInfInformation, SetupGetInfInformation function [Setup API], SetupGetInfInformationA, SetupGetInfInformationW, _setupapi_setupgetinfinformation, setup.setupgetinfinformation, setupapi/SetupGetInfInformation, setupapi/SetupGetInfInformationA, setupapi/SetupGetInfInformationW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetInfInformationW (Unicode) and SetupGetInfInformationA (ANSI)
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
 - SetupGetInfInformationA
 - setupapi/SetupGetInfInformationA
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
 - SetupGetInfInformation
 - SetupGetInfInformationA
 - SetupGetInfInformationW
---

# SetupGetInfInformationA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetUpGetInfInformation</b> function returns the 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_inf_information">SP_INF_INFORMATION</a> structure for the specified INF file to a buffer.

## -parameters

### -param InfSpec [in]

Handle or a file name for an INF file, depending on the value of <i>SearchControl</i>.

### -param SearchControl [in]

This parameter can be one of the following constants. 







#### INFINFO_INF_SPEC_IS_HINF

<i>InfSpec</i> is an INF handle. A single INF handle may reference multiple INF files if they have been append-loaded together. If it does, the structure returned by this function contains multiple sets of information.



#### INFINFO_INF_NAME_IS_ABSOLUTE

The string specified for <i>InfSpec</i> is a full path. No further processing is performed on <i>InfSpec</i>.



#### INFINFO_DEFAULT_SEARCH

Search the default locations for the INF file specified for <i>InfSpec</i>, which is assumed to be a filename only. The default locations are <i>%windir%</i>&#92;<i>inf</i>, followed by <i>%windir%</i>&#92;<i>system32</i>.



#### INFINFO_REVERSE_DEFAULT_SEARCH

Same as INFINFO_DEFAULT_SEARCH, except the default locations are searched in reverse order.



#### INFINFO_INF_PATH_LIST_SEARCH

Search for the INF in each of the directories listed in the <i>DevicePath</i> value entry under the following:<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion</b>

### -param ReturnBuffer [in, out]

If not <b>NULL</b>, points to a buffer in which this function returns the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_inf_information">SP_INF_INFORMATION</a> structure. 

You can call the function one time to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. For more information, see the Remarks section of this topic.

### -param ReturnBufferSize [in]

Size of  <i>ReturnBuffer</i>, in bytes.

### -param RequiredSize [in, out]

If not <b>NULL</b>, points to a variable in which this function returns the required size, in bytes, for the buffer pointed to by <i>ReturnBuffer</i>. 

If <i>ReturnBuffer</i> is specified and the size needed is larger than <i>ReturnBufferSize</i>, the function fails and a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the INF file cannot be located, the function returns <b>FALSE</b> and a subsequent call to 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_FILE_NOT_FOUND.

## -remarks

If this function is called with a ReturnBuffer of <b>NULL</b> and a ReturnBufferSize of 0 (zero), the function puts the buffer size needed to hold the specified data into the variable pointed to by RequiredSize. If the function succeeds, the return value is a nonzero value. Otherwise, the return value is 0 (zero), and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.





> [!NOTE]
> The setupapi.h header defines SetupGetInfInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueryinffileinformationa">SetupQueryInfFileInformation</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueryinfversioninformationa">SetupQueryInfVersionInformation</a>
