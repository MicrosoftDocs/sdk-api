---
UID: NF:wtsapi32.WTSVirtualChannelQuery
title: WTSVirtualChannelQuery function (wtsapi32.h)
description: Returns information about a specified virtual channel.
helpviewer_keywords: ["WTSVirtualChannelQuery","WTSVirtualChannelQuery function [Remote Desktop Services]","_win32_wtsvirtualchannelquery","termserv.wtsvirtualchannelquery","wtsapi32/WTSVirtualChannelQuery"]
old-location: termserv\wtsvirtualchannelquery.htm
tech.root: TermServ
ms.assetid: 68ae8174-d72b-4b1c-b8e9-ae5fed51d385
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelQuery, WTSVirtualChannelQuery function [Remote Desktop Services], _win32_wtsvirtualchannelquery, termserv.wtsvirtualchannelquery, wtsapi32/WTSVirtualChannelQuery
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
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSVirtualChannelQuery
 - wtsapi32/WTSVirtualChannelQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSVirtualChannelQuery
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSVirtualChannelQuery function


## -description

Returns information about a specified virtual 
    channel.

## -parameters

### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a> function.

### -param WTS_VIRTUAL_CLASS [in]

Specifies the type of information returned in the <i>ppBuffer</i> parameter. This parameter 
      can be a value from the <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_virtual_class">WTS_VIRTUAL_CLASS</a> 
      enumeration type.

### -param ppBuffer [out]

Pointer to a buffer that receives the requested information.

### -param pBytesReturned [out]

Pointer to a variable that receives the number of bytes returned in the <i>ppBuffer</i> 
      parameter.

## -returns

If the function succeeds, the return value is a nonzero value. Call the 
       <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> function with the value returned in 
       the <i>ppBuffer</i> parameter to free the temporary memory allocated by 
       <b>WTSVirtualChannelQuery</b>.
      

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The following example shows how to gain access to a virtual channel file handle that can be used for 
    asynchronous I/O. First the code opens a virtual channel by using a call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a> function.
    Then the code calls the 
    <b>WTSVirtualChannelQuery</b> function, specifying 
    the WTSVirtualFileHandle virtual class type. 
    <b>WTSVirtualChannelQuery</b> returns a file 
    handle that you can use to perform asynchronous (overlapped) read and write operations. Finally, the code frees 
    the memory allocated by 
    <b>WTSVirtualChannelQuery</b> with a call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> function, and closes the 
    virtual channel with a call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelclose">WTSVirtualChannelClose</a> function.

Note that you should not explicitly close the file handle obtained by calling 
    <b>WTSVirtualChannelQuery</b>. This is because 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelclose">WTSVirtualChannelClose</a> closes the file handle.


```cpp
    PVOID vcFileHandlePtr = NULL;
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
                            &vcFileHandlePtr,
                            &len
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
        memcpy(&vcFileHandle, vcFileHandlePtr, sizeof(vcFileHandle));
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

```


For more information about overlapped mode, see 
    <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and 
    Output</a>.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a>



<a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_virtual_class">WTS_VIRTUAL_CLASS</a>
