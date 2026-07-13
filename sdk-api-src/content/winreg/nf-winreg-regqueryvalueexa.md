---
UID: NF:winreg.RegQueryValueExA
title: RegQueryValueExA function (winreg.h)
description: Retrieves the type and data for the specified value name associated with an open registry key. (ANSI)
helpviewer_keywords: ["RegQueryValueExA", "winreg/RegQueryValueExA"]
old-location: base\regqueryvalueex.htm
tech.root: winprog
ms.assetid: 202d253a-10ff-40e7-8eec-a49717443b81
ms.date: 12/05/2018
ms.keywords: RegQueryValueEx, RegQueryValueEx function, RegQueryValueExA, RegQueryValueExW, _win32_regqueryvalueex, base.regqueryvalueex, winreg/RegQueryValueEx, winreg/RegQueryValueExA, winreg/RegQueryValueExW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegQueryValueExW (Unicode) and RegQueryValueExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegQueryValueExA
 - winreg/RegQueryValueExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
 - kernel32.dll
api_name:
 - RegQueryValueEx
 - RegQueryValueExA
 - RegQueryValueExW
---

# RegQueryValueExA function


## -description

Retrieves the type and data for the specified value name associated with an open registry key.

> [!WARNING]
> If the value being queried is a string (REG_SZ, REG_MULTI_SZ, and REG_EXPAND_SZ) the value returned is NOT guaranteed to be null-terminated. Use the <a href="/windows/desktop/api/winreg/nf-winreg-reggetvaluea">RegGetValue</a> function if you want to ensure returned string values are null-terminated. More information is in the remarks below.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_PERFORMANCE_DATA</b></dd>
<dd><b>HKEY_PERFORMANCE_NLSTEXT</b></dd>
<dd><b>HKEY_PERFORMANCE_TEXT</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param lpValueName [in, optional]

The name of the registry value. 




If <i>lpValueName</i> is <b>NULL</b> or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any. 

If <i>lpValueName</i> specifies a value that is not in the registry, the function returns ERROR_FILE_NOT_FOUND.

Keys do not automatically have an unnamed or default value. Unnamed values can be of any type. For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.

### -param lpType [out, optional]

A pointer to a variable that receives a code indicating the type of data stored in the specified value. For a list of the possible type codes, see 
<a href="/windows/desktop/SysInfo/registry-value-types">Registry Value Types</a>. The <i>lpType</i> parameter can be <b>NULL</b> if the type code is not required.

### -param lpData [out, optional]

A pointer to a buffer that receives the value's data. This parameter can be <b>NULL</b> if the data is not required.

### -param lpcbData [in, out, optional]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpData</i> parameter, in bytes. When the function returns, this variable contains the size of the data copied to <i>lpData</i>. 




The <i>lpcbData</i> parameter can be <b>NULL</b> only if <i>lpData</i> is <b>NULL</b>.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, this size includes any terminating <b>null</b> character or characters unless the data was stored without them. For more information, see Remarks.

If the buffer specified by <i>lpData</i> parameter is not large enough to hold the data, the function returns ERROR_MORE_DATA and stores the required buffer size in the variable pointed to by <i>lpcbData</i>. In this case, the contents of the <i>lpData</i> buffer are undefined.

If <i>lpData</i> is <b>NULL</b>, and <i>lpcbData</i> is non-<b>NULL</b>, the function returns ERROR_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by <i>lpcbData</i>. This enables an application to determine the best way to allocate a buffer for the value's data.

If <i>hKey</i> specifies <b>HKEY_PERFORMANCE_DATA</b> and the <i>lpData</i> buffer is not large enough to contain all of the returned data, 
<b>RegQueryValueEx</b> returns ERROR_MORE_DATA and the value returned through the <i>lpcbData</i> parameter is undefined. This is because the size of the performance data can change from one call to the next. In this case, you must increase the buffer size and call 
<b>RegQueryValueEx</b> again passing the updated buffer size in the <i>lpcbData</i> parameter. Repeat this until the function succeeds. You need to maintain a separate variable to keep track of the buffer size, because the value returned by <i>lpcbData</i> is unpredictable.

If the <i>lpValueName</i> registry value does not exist, <b>RegQueryValueEx</b> returns ERROR_FILE_NOT_FOUND and the value returned through the <i>lpcbData</i> parameter is undefined.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

If the <i>lpData</i> buffer is too small to receive the data, the function returns ERROR_MORE_DATA.

If the <i>lpValueName</i> registry value does not exist, the function returns ERROR_FILE_NOT_FOUND.

## -remarks

An application typically calls <a href="/windows/desktop/api/winreg/nf-winreg-regenumvaluea">RegEnumValue</a> to determine the value names and then <b>RegQueryValueEx</b> to retrieve the data for the names.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, the string may not have been stored with the proper terminating <b>null</b> characters. Therefore, even if the function returns ERROR_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer. (Note that REG_MULTI_SZ strings should have two terminating <b>null</b> characters.) One way an application can ensure that the string is properly terminated is to use <a href="/windows/desktop/api/winreg/nf-winreg-reggetvaluea">RegGetValue</a>, which adds terminating <b>null</b> characters if needed.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, and the ANSI version of this function is used (either by explicitly calling <b>RegQueryValueExA</b> or by not defining UNICODE before including the Windows.h file), this function converts the stored Unicode string to an ANSI string before copying it to the buffer pointed to by <i>lpData</i>.

When calling the 
<b>RegQueryValueEx</b> function with <i>hKey</i> set to the <b>HKEY_PERFORMANCE_DATA</b> handle and a value string of a specified object, the returned data structure sometimes has unrequested objects. Do not be surprised; this is normal behavior. When calling the 
<b>RegQueryValueEx</b> function, you should always expect to walk the returned data structure to look for the requested object.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="/windows/desktop/SysInfo/registry-virtualization">Registry Virtualization</a> and <a href="/windows/desktop/SysInfo/32-bit-and-64-bit-application-data-in-the-registry">32-bit and 64-bit Application Data in the Registry</a>.


#### Examples

Ensure that you reinitialize the value  pointed to by the <i>lpcbData</i> parameter each time  you  call this function. This is very important when you call this function in a loop, as in the following code example.


```cpp
#include <windows.h>
#include <malloc.h>
#include <stdio.h>

#define TOTALBYTES    8192
#define BYTEINCREMENT 4096

void main()
{
    DWORD BufferSize = TOTALBYTES;
    DWORD cbData;
    DWORD dwRet;

    PPERF_DATA_BLOCK PerfData = (PPERF_DATA_BLOCK) malloc( BufferSize );
    cbData = BufferSize;

    printf("\nRetrieving the data...");

    dwRet = RegQueryValueEx( HKEY_PERFORMANCE_DATA,
                             TEXT("Global"),
                             NULL,
                             NULL,
                             (LPBYTE) PerfData,
                             &cbData );
    while( dwRet == ERROR_MORE_DATA )
    {
        // Get a buffer that is big enough.

        BufferSize += BYTEINCREMENT;
        PerfData = (PPERF_DATA_BLOCK) realloc( PerfData, BufferSize );
        cbData = BufferSize;

        printf(".");
        dwRet = RegQueryValueEx( HKEY_PERFORMANCE_DATA,
                         TEXT("Global"),
                         NULL,
                         NULL,
                         (LPBYTE) PerfData,
                         &cbData );
    }
    if( dwRet == ERROR_SUCCESS )
        printf("\n\nFinal buffer size is %d\n", BufferSize);
    else printf("\nRegQueryValueEx failed (%d)\n", dwRet);
}

```






> [!NOTE]
> The winreg.h header defines RegQueryValueEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">ExpandEnvironmentStrings</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumkeyexa">RegEnumKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumvaluea">RegEnumValue</a>



<a href="/windows/desktop/api/winreg/nf-winreg-reggetvaluea">RegGetValue</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
