---
UID: NF:ras.RasGetErrorStringW
title: RasGetErrorStringW function
author: windows-sdk-content
description: The RasGetErrorString function obtains an error message string for a specified RAS error value.
old-location: rras\rasgeterrorstring.htm
old-project: rras
ms.assetid: 4d308dd8-e623-467b-836e-faace19460f1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasGetErrorString, RasGetErrorString function [RAS], RasGetErrorStringA, RasGetErrorStringW, _ras_rasgeterrorstring, ras/RasGetErrorString, ras/RasGetErrorStringA, ras/RasGetErrorStringW, rras.rasgeterrorstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ras.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
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
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasGetErrorStringW function


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

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h. There is no <a href="https://msdn.microsoft.com/en-us/library/ms629690(v=VS.85).aspx">GetLastError</a> information set by the 
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





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa366574(v=VS.85).aspx">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647486(v=VS.85).aspx">LoadString</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

