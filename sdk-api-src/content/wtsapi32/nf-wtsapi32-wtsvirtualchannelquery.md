---
UID: NF:wtsapi32.WTSVirtualChannelQuery
title: WTSVirtualChannelQuery function
author: windows-sdk-content
description: Returns information about a specified virtual channel.
old-location: termserv\wtsvirtualchannelquery.htm
old-project: termserv
ms.assetid: 68ae8174-d72b-4b1c-b8e9-ae5fed51d385
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WTSVirtualChannelQuery, WTSVirtualChannelQuery function [Remote Desktop Services], _win32_wtsvirtualchannelquery, termserv.wtsvirtualchannelquery, wtsapi32/WTSVirtualChannelQuery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSVirtualChannelQuery
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSVirtualChannelQuery function


## -description


Returns information about a specified virtual 
    channel.


## -parameters




### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
      <a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a> function.


### -param WTS_VIRTUAL_CLASS

TBD


### -param ppBuffer [out]

Pointer to a buffer that receives the requested information.


### -param pBytesReturned [out]

Pointer to a variable that receives the number of bytes returned in the <i>ppBuffer</i> 
      parameter.


#### - WtsVirtualClass [in]

Specifies the type of information returned in the <i>ppBuffer</i> parameter. This parameter 
      can be a value from the <a href="https://msdn.microsoft.com/ca7bb0ff-f5af-477f-a610-563071554234">WTS_VIRTUAL_CLASS</a> 
      enumeration type.


## -returns




       If the function succeeds, the return value is a nonzero value. Call the 
       <a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a> function with the value returned in 
       the <i>ppBuffer</i> parameter to free the temporary memory allocated by 
       <b>WTSVirtualChannelQuery</b>.
      


       If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
      




## -remarks



The following example shows how to gain access to a virtual channel file handle that can be used for 
    asynchronous I/O. First the code opens a virtual channel by using a call to the 
    <a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a> function.
    Then the code calls the 
    <b>WTSVirtualChannelQuery</b> function, specifying 
    the WTSVirtualFileHandle virtual class type. 
    <b>WTSVirtualChannelQuery</b> returns a file 
    handle that you can use to perform asynchronous (overlapped) read and write operations. Finally, the code frees 
    the memory allocated by 
    <b>WTSVirtualChannelQuery</b> with a call to the 
    <a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a> function, and closes the 
    virtual channel with a call to the 
    <a href="https://msdn.microsoft.com/d82cb1cd-a9bd-45e8-8a86-2c7dd860b987">WTSVirtualChannelClose</a> function.

Note that you should not explicitly close the file handle obtained by calling 
    <b>WTSVirtualChannelQuery</b>. This is because 
    <a href="https://msdn.microsoft.com/d82cb1cd-a9bd-45e8-8a86-2c7dd860b987">WTSVirtualChannelClose</a> closes the file handle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    PVOID vcFileHandlePtr = NULL;
    DWORD len;
    DWORD result = ERROR_SUCCESS;
    HANDLE vcHandle = NULL;
    HANDLE vcFileHandle = NULL;

    //
    //  Open a virtual channel.
    //
    vcHandle = WTSVirtualChannelOpen(
                      WTS_CURRENT_SERVER_HANDLE, // Current TS Server
                      WTS_CURRENT_SESSION,       // Current TS Session
                      (LPSTR) "TSTCHNL"                 // Channel name
                      );

    if (vcHandle == NULL) 
    {
        result = GetLastError();
    }

    //
    //  Gain access to the underlying file handle for 
    //   asynchronous I/O. 
    //
    if (result == ERROR_SUCCESS) 
    {
        if (!WTSVirtualChannelQuery(
                            vcHandle,
                            WTSVirtualFileHandle,
                            &amp;vcFileHandlePtr,
                            &amp;len
                            )) 
        {
            result = GetLastError();
        }
    }

    //
    //  Copy the data and
    //   free the buffer allocated by WTSVirtualChannelQuery.
    //
    if (result == ERROR_SUCCESS) 
    {
        memcpy(&amp;vcFileHandle, vcFileHandlePtr, sizeof(vcFileHandle));
        WTSFreeMemory(vcFileHandlePtr);

        //
        //  Use vcFileHandle for overlapped reads and writes here.
        //
        //.
        //.
        //.
    }

    //
    //  Call WTSVirtualChannelClose to close the virtual channel. 
    //   Note: do not close the file handle.
    //
    if (vcHandle != NULL) 
    {
        WTSVirtualChannelClose(vcHandle);
        vcFileHandle = NULL;
    }
</pre>
</td>
</tr>
</table></span></div>
For more information about overlapped mode, see 
    <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and 
    Output</a>.




## -see-also




<a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a>



<a href="https://msdn.microsoft.com/ca7bb0ff-f5af-477f-a610-563071554234">WTS_VIRTUAL_CLASS</a>
 

 

