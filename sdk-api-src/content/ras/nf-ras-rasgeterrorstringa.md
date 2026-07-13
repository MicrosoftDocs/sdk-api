---
UID: NF:ras.RasGetErrorStringA
title: RasGetErrorStringA function (ras.h)
description: The RasGetErrorString function obtains an error message string for a specified RAS error value. (ANSI)
helpviewer_keywords: ["RasGetErrorStringA", "ras/RasGetErrorStringA"]
old-location: rras\rasgeterrorstring.htm
tech.root: RRAS
ms.assetid: 4d308dd8-e623-467b-836e-faace19460f1
ms.date: 12/05/2018
ms.keywords: RasGetErrorString, RasGetErrorString function [RAS], RasGetErrorStringA, RasGetErrorStringW, _ras_rasgeterrorstring, ras/RasGetErrorString, ras/RasGetErrorStringA, ras/RasGetErrorStringW, rras.rasgeterrorstring
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetErrorStringW (Unicode) and RasGetErrorStringA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasGetErrorStringA
 - ras/RasGetErrorStringA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasGetErrorString
 - RasGetErrorStringA
 - RasGetErrorStringW
---

# RasGetErrorStringA function


## -description

The 
<b>RasGetErrorString</b> function obtains an error message string for a specified RAS error value.

## -parameters

### -param ResourceId [in]

Specifies the error value of interest. These are values returned by one of the RAS functions: those listed in the RasError.h header file.

### -param lpszString [out]

Pointer to a buffer that receives the error string. This parameter must not be <b>NULL</b>.

### -param InBufSize [in]

Specifies the size, in characters, of the buffer pointed to by <i>lpszErrorString</i>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h. There is no <a href="/previous-versions/windows/desktop/wab/-wab-iabcontainer-getlasterror">GetLastError</a> information set by the 
<b>RasGetErrorString</b> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed into the function.

</td>
</tr>
</table>

## -remarks

There is no way to determine in advance the exact size in characters of an error message, and thus the size of buffer required. Error messages will generally be 80 characters or fewer in size; a buffer size of 512 characters will always be adequate. A buffer of insufficient size causes the 
<b>RasGetErrorString</b> function to fail, returning <b>ERROR_INSUFFICIENT_BUFFER</b>. Note that buffer sizes are specified in characters, not bytes; thus, the Unicode version of 
<b>RasGetErrorString</b> requires at least a  1024 byte buffer to guarantee that every error message  fits.


#### Examples

The following code obtains an error string for the RAS error 633.


```cpp

#include <windows.h>
#include <stdio.h>
#include "ras.h"
#include "rasdlg.h"
#include <tchar.h>

#define  ERROR_VAL 633
#define  BUFFER_SIZE 256

DWORD __cdecl wmain(){

    DWORD dwRetVal = ERROR_SUCCESS;
    UINT  uErrorValue = ERROR_VAL;
    DWORD cBufSize = BUFFER_SIZE;
    WCHAR lpszErrorString[BUFFER_SIZE];

    dwRetVal = RasGetErrorString(uErrorValue, lpszErrorString, cBufSize);

    if(dwRetVal == ERROR_SUCCESS){
        wprintf(L"Error Code %d: %s\n", uErrorValue, lpszErrorString);
    }else{
           wprintf(L"RasGetErrorString failed, Return Value: %d", dwRetVal);
    }

    return 0;
}

```






> [!NOTE]
> The ras.h header defines RasGetErrorString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
