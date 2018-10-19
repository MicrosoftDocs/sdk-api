---
UID: NF:winreg.RegQueryValueExW
title: RegQueryValueExW function
author: windows-sdk-content
description: Retrieves the type and data for the specified value name associated with an open registry key.
old-location: base\regqueryvalueex.htm
tech.root: sysinfo
ms.assetid: 202d253a-10ff-40e7-8eec-a49717443b81
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: RegQueryValueEx, RegQueryValueEx function, RegQueryValueExA, RegQueryValueExW, _win32_regqueryvalueex, base.regqueryvalueex, winreg/RegQueryValueEx, winreg/RegQueryValueExA, winreg/RegQueryValueExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegQueryValueExW function


## -description


Retrieves the type and data for the specified value name associated with an open registry key.

To ensure that any string values (REG_SZ, REG_MULTI_SZ, and REG_EXPAND_SZ) returned are <b>null</b>-terminated, use the <a href="https://msdn.microsoft.com/1c06facb-6735-4b3f-b77d-f162e3faaada">RegGetValue</a> function.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, or 
<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:<dl>
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
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.


### -param lpType [out, optional]

A pointer to a variable that receives a code indicating the type of data stored in the specified value. For a list of the possible type codes, see 
<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>. The <i>lpType</i> parameter can be <b>NULL</b> if the type code is not required.


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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.

If the <i>lpData</i> buffer is too small to receive the data, the function returns ERROR_MORE_DATA.

If the <i>lpValueName</i> registry value does not exist, the function returns ERROR_FILE_NOT_FOUND.




## -remarks



An application typically calls <a href="https://msdn.microsoft.com/7014ff96-c655-486f-af32-180b87281b06">RegEnumValue</a> to determine the value names and then <b>RegQueryValueEx</b> to retrieve the data for the names.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, the string may not have been stored with the proper terminating <b>null</b> characters. Therefore, even if the function returns ERROR_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer. (Note that REG_MULTI_SZ strings should have two terminating <b>null</b> characters.) One way an application can ensure that the string is properly terminated is to use <a href="https://msdn.microsoft.com/1c06facb-6735-4b3f-b77d-f162e3faaada">RegGetValue</a>, which adds terminating <b>null</b> characters if needed.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, and the ANSI version of this function is used (either by explicitly calling <b>RegQueryValueExA</b> or by not defining UNICODE before including the Windows.h file), this function converts the stored Unicode string to an ANSI string before copying it to the buffer pointed to by <i>lpData</i>.

When calling the 
<b>RegQueryValueEx</b> function with <i>hKey</i> set to the <b>HKEY_PERFORMANCE_DATA</b> handle and a value string of a specified object, the returned data structure sometimes has unrequested objects. Do not be surprised; this is normal behavior. When calling the 
<b>RegQueryValueEx</b> function, you should always expect to walk the returned data structure to look for the requested object.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="https://msdn.microsoft.com/dace2f65-df60-419a-8be8-ab60668e6396">Registry Virtualization</a> and <a href="https://msdn.microsoft.com/08dc034c-15ce-41d9-8e74-a49b61ad40a6">32-bit and 64-bit Application Data in the Registry</a>.


#### Examples

Ensure that you reinitialize the value  pointed to by the <i>lpcbData</i> parameter each time  you  call this function. This is very important when you call this function in a loop, as in the following code example.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;malloc.h&gt;
#include &lt;stdio.h&gt;

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
                             &amp;cbData );
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
                         &amp;cbData );
    }
    if( dwRet == ERROR_SUCCESS )
        printf("\n\nFinal buffer size is %d\n", BufferSize);
    else printf("\nRegQueryValueEx failed (%d)\n", dwRet);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b563e8ed-311d-4971-94f3-9c9fde4a2f30">ExpandEnvironmentStrings</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/647d34cc-01ba-4389-be29-b099ed198e7c">RegEnumKeyEx</a>



<a href="https://msdn.microsoft.com/7014ff96-c655-486f-af32-180b87281b06">RegEnumValue</a>



<a href="https://msdn.microsoft.com/1c06facb-6735-4b3f-b77d-f162e3faaada">RegGetValue</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

