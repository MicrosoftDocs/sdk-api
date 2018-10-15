---
UID: NF:lmshare.NetConnectionEnum
title: NetConnectionEnum function
author: windows-sdk-content
description: Lists all connections made to a shared resource on the server or all connections established from a particular computer.
old-location: fs\netconnectionenum.htm
tech.root: NetShare
ms.assetid: 935ac6e9-78e0-42ae-a454-0a14b03ddc21
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 0, 1, NetConnectionEnum, NetConnectionEnum function [Files], _win32_netconnectionenum, fs.netconnectionenum, lmshare/NetConnectionEnum, netmgmt.netconnectionenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmshare.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetConnectionEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetConnectionEnum function


## -description


Lists all connections made to a shared resource on the server or all connections established from a particular computer. If there is more than one user using this connection, then it is possible to get more than one structure for the same connection, but with a different user name.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.


### -param qualifier [in]

Pointer to a string that specifies a share name or computer name for the connections of interest. If it is a share name, then all the connections made to that share name are listed. If it is a computer name (for example, it starts with two backslash characters), then 
<b>NetConnectionEnum</b> lists all connections made from that computer to the server specified.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
 Return connection identifiers. The <i>bufptr</i> parameter is a pointer to an array of 
<a href="https://msdn.microsoft.com/aebafe24-1216-48ab-92db-df8f77d36f26">CONNECTION_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
 Return connection identifiers and connection information. The <i>bufptr</i> parameter is a pointer to an array of 
<a href="https://msdn.microsoft.com/9904c448-dcc4-47cc-a2e0-7df8d4d37f3f">CONNECTION_INFO_1</a> structures.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the address of the buffer that receives the information. The format of this data depends on the value of the <i>level</i> parameter. 




This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with <b>ERROR_MORE_DATA</b>.


### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify <b>MAX_PREFERRED_LENGTH</b>, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns <b>ERROR_MORE_DATA</b>. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.


### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.


### -param resume_handle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing connection search. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, then no resume handle is stored.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Administrator, Server or Print Operator, or Power User group membership is required to successfully execute the 
<b>NetConnectionEnum</b> function.


#### Examples

The following code sample demonstrates how to list the connections made to a shared resource with a call to the 
<b>NetConnectionEnum</b> function. The sample calls 
<b>NetConnectionEnum</b>, specifying information level 1 (<a href="https://msdn.microsoft.com/9904c448-dcc4-47cc-a2e0-7df8d4d37f3f">CONNECTION_INFO_1</a>). If there are entries to return, it prints the values of the <b>coni1_username</b> and <b>coni1_netname</b> members. If there are no entries to return, the sample prints an appropriate message. Finally, the code sample frees the memory allocated for the information buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#include &lt;windows.h&gt;
#include &lt;lm.h&gt;
#include &lt;stdio.h&gt;
#pragma comment(lib, "Netapi32.lib")

void wmain(int argc, wchar_t *argv[ ])
{
   DWORD res, i, er = 0, tr = 0, resume = 0;
   PCONNECTION_INFO_1 p,b;
   LPTSTR lpszServer = NULL, lpszShare = NULL;

   if(argc&lt;2)
      wprintf(L"Syntax: %s [ServerName] ShareName | \\\\ComputerName\n", argv[0]);
   else
   {
      //
      // The server is not the default local computer.
      //
      if(argc&gt;2)
         lpszServer=argv[1];
      //
      // ShareName is always the last argument.
      //
      lpszShare=argv[argc - 1];
      //
      // Call the NetConnectionEnum function,
      //  specifying information level 1.
      //
      res=NetConnectionEnum(lpszServer, lpszShare, 1, (LPBYTE *) &amp;p, MAX_PREFERRED_LENGTH, &amp;er, &amp;tr, &amp;resume);
      //
      // If no error occurred,
      //
      if(res == 0)
      {
         //
         // If there were any results,
         //
         if(er&gt;0)
         {
            b=p;
            //
            // Loop through the entries; print user name and network name.
            //
            for(i=0;i&lt;er;i++)
            {
               printf("%S\t%S\n", b-&gt;coni1_username,b-&gt;coni1_netname);
               b++;
            }
            // Free the allocated buffer.
            //
            NetApiBufferFree(p);
         }
         // Otherwise, print a message depending on whether 
         //  the qualifier parameter was a computer (\\ComputerName)
         //  or a share (ShareName).
         //
         else
         {
            if(lpszShare[0]=='\\')  
               printf("No connection to %S from %S\n", 
                  (lpszServer == NULL)?TEXT("LocalMachine"):lpszServer, lpszShare);
            else                       
               printf("No one connected to %S\\%S\n",
                  (lpszServer == NULL)?TEXT("\\\\LocalMachine"):lpszServer,lpszShare);
         }        
      }
      //
      // Otherwise, print the error.
      //
      else
         printf("Error: %d\n",res);
   }
   return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/aebafe24-1216-48ab-92db-df8f77d36f26">CONNECTION_INFO_0</a>



<a href="https://msdn.microsoft.com/9904c448-dcc4-47cc-a2e0-7df8d4d37f3f">CONNECTION_INFO_1</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

