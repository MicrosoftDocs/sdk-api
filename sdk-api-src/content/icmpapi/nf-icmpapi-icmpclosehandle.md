---
UID: NF:icmpapi.IcmpCloseHandle
title: IcmpCloseHandle function
author: windows-sdk-content
description: The IcmpCloseHandle function closes a handle opened by a call to the IcmpCreateFile or Icmp6CreateFile functions.
old-location: iphlp\icmpclosehandle.htm
old-project: IpHlp
ms.assetid: ce8f11bb-1e33-41bd-adb9-c18efadd4d0b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IcmpCloseHandle, IcmpCloseHandle function [IP Helper], _iphlp_icmpclosehandle, icmpapi/IcmpCloseHandle, iphlp.icmpclosehandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
-	Icmp.dll
api_name:
-	IcmpCloseHandle
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP; Icmp.dll on Windows 2000 Server and Windows 2000 Professional
req.irql: 
req.product: GDI+ 1.1
---

# IcmpCloseHandle function


## -description


The 
<b>IcmpCloseHandle</b> function closes a handle opened by a call to 
the <a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a> or <a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a> functions.


## -parameters




### -param IcmpHandle [in]

The handle to close. This handle must have been returned by a call to <a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a> or <a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>.


## -returns



If the handle is closed successfully the return value is <b>TRUE</b>, otherwise <b>FALSE</b>. Call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for extended error information.




## -remarks



The <b>IcmpCloseHandle</b> function is exported from the <i>Icmp.dll</i> on Windows 2000. The <b>IcmpCloseHandle</b> function is exported from the <i>Iphlpapi.dll</i> on Windows XP and later. Windows version checking is not recommended to use this function. Applications requiring portability  with this function across Windows 2000, Windows XP, Windows Server 2003 and later Windows versions should not statically link to either the <i>Icmp.lib</i> or the <i>Iphlpapi.lib</i> file. Instead, the application should check for the presence of <b>IcmpCloseHandle</b> in the <i>Iphlpapi.dll</i> with calls to <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.  Failing that, the application should check for the presence of <b>IcmpCloseHandle</b> in the <i>Icmp.dll</i> with  calls to <b>LoadLibrary</b> and <b>GetProcAddress</b>. 

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.


#### Examples

The following example opens and closes a handle on which ICMP echo requests can be issued. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;icmpapi.h&gt;
#include &lt;stdio.h&gt;

#pragma comment(lib, "iphlpapi.lib")

void main()
{
    HANDLE hIcmpFile;
    BOOL bRetVal; 

    hIcmpFile = IcmpCreateFile();
    if (hIcmpFile == INVALID_HANDLE_VALUE)
      printf("IcmpCreateFile failed with error: %ld\n", GetLastError() );
    else 
    {
      printf("\tHandle created.\n");

      bRetVal = IcmpCloseHandle(hIcmpFile);
      if (bRetVal)
          printf("\tHandle was closed\n");
      else
          printf("IcmpCloseHandle failed with error: %ld\n", GetLastError() );
    }
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>



<a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a>



<a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>



<a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a>



<a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a>



<b>IcmpSendEcho</b>



<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>



<a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>
 

 

