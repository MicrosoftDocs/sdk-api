---
UID: NF:setupapi.SetupGetIntField
title: SetupGetIntField function (setupapi.h)
description: The SetupGetIntField function retrieves an integer value from the specified field of a line in an INF file.
helpviewer_keywords: ["SetupGetIntField","SetupGetIntField function [Setup API]","_setupapi_setupgetintfield","setup.setupgetintfield","setupapi/SetupGetIntField"]
old-location: setup\setupgetintfield.htm
tech.root: setup
ms.assetid: 4c77052a-46ef-4154-82c0-5ec447861bcf
ms.date: 12/05/2018
ms.keywords: SetupGetIntField, SetupGetIntField function [Setup API], _setupapi_setupgetintfield, setup.setupgetintfield, setupapi/SetupGetIntField
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
 - SetupGetIntField
 - setupapi/SetupGetIntField
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
 - SetupGetIntField
req.apiset: ext-ms-win-setupapi-inf-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetupGetIntField function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetIntField</b> function retrieves an integer value from the specified field of a line in an INF file.

## -parameters

### -param Context [in]

Pointer to the context for a line in an INF file.

### -param FieldIndex [in]

The 1-based index of the field within the specified line from which the integer should be retrieved. 




A <i>FieldIndex</i> of 0 can be used to retrieve an integer key (For example, consider the following INF line, 431 = 1, 2, 4. The value 431 would be put into the variable pointed at by <i>IntegerValue</i> if 
<b>SetupGetIntField</b> was called with a <i>FieldIndex</i> of 0).

### -param IntegerValue [out]

Pointer to a variable that receives the integer. If the field is not an integer, the function fails and a call to 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_DATA.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The integer field may start with a positive (+) or negative (-) sign. It will be interpreted as a decimal number, unless  prefixed in the file with 0x or 0X, in which case it is hexadecimal.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetbinaryfield">SetupGetBinaryField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetmultiszfielda">SetupGetMultiSzField</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetstringfielda">SetupGetStringField</a>
