---
UID: NF:winbase.GetComputerNameA
title: GetComputerNameA function
author: windows-sdk-content
description: Retrieves the NetBIOS name of the local computer. This name is established at system startup, when the system reads it from the registry.
old-location: base\getcomputername.htm
tech.root: sysinfo
ms.assetid: 8ca3e611-e5fb-4909-adf6-98eb8552c9e1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetComputerName, GetComputerName function, GetComputerNameA, GetComputerNameW, _win32_getcomputername, base.getcomputername, winbase/GetComputerName, winbase/GetComputerNameA, winbase/GetComputerNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetComputerNameW (Unicode) and GetComputerNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetComputerName
 - GetComputerNameA
 - GetComputerNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetComputerNameA function


## -description


Retrieves the NetBIOS name of the local computer. This name is established at system startup, when the system reads it from the registry.

<b>GetComputerName</b> retrieves only the NetBIOS name of the local computer. To retrieve the DNS host name, DNS domain name, or the fully qualified DNS name, call the 
<a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a> function. Additional information is provided by the 
<a href="https://msdn.microsoft.com/5573d37b-10a8-4176-80c7-711552ff36cb">IADsADSystemInfo</a> interface.

The behavior of this function can be affected if the local computer is a node in a cluster. For more information, see <a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a> and <a href="https://msdn.microsoft.com/3ef0eb0b-1472-450d-aa08-6622a7475793">UseNetworkName</a>.


## -parameters




### -param lpBuffer [out]

A pointer to a buffer that receives the computer name or the cluster virtual server name. The buffer size should be large enough to contain MAX_COMPUTERNAME_LENGTH + 1 characters.


### -param nSize [in, out]

On input, specifies the size of the buffer, in <b>TCHARs</b>. On output, the number of <b>TCHARs</b> copied to the destination buffer, not including the terminating null character. 




If the buffer is too small, the function fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_BUFFER_OVERFLOW. The <i>lpnSize</i> parameter specifies the size of the buffer required, including the terminating null character.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetComputerName</b> function retrieves the NetBIOS name established at system startup. Name changes made by the 
<a href="https://msdn.microsoft.com/ff64fde2-d1b5-4211-b8c4-4823a5469e04">SetComputerName</a> or 
<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a> functions do not take effect until the user restarts the computer.

If the caller is running under a client session, this function returns the server name. To retrieve the client name, use the <a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/965bd14b-be93-4084-bce8-642f5704cef1">Getting System Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7e083cb5-cf0a-4284-8b54-dac856910c44">Computer Names</a>



<a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a>



<a href="https://msdn.microsoft.com/ff64fde2-d1b5-4211-b8c4-4823a5469e04">SetComputerName</a>



<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
    Information Functions</a>
 

 

