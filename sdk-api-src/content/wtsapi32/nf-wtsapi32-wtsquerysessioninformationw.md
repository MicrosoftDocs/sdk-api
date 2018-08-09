---
UID: NF:wtsapi32.WTSQuerySessionInformationW
title: WTSQuerySessionInformationW function
author: windows-sdk-content
description: Retrieves session information for the specified session on the specified Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtsquerysessioninformation.htm
old-project: termserv
ms.assetid: d52345a4-0408-4ea9-ba71-349910143752
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WTSQuerySessionInformation, WTSQuerySessionInformation function [Remote Desktop Services], WTSQuerySessionInformationA, WTSQuerySessionInformationW, _win32_wtsquerysessioninformation, termserv.wtsquerysessioninformation, wtsapi32/WTSQuerySessionInformation, wtsapi32/WTSQuerySessionInformationA, wtsapi32/WTSQuerySessionInformationW
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
req.unicode-ansi: WTSQuerySessionInformationW (Unicode) and WTSQuerySessionInformationA (ANSI)
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
 - WTSQuerySessionInformation
 - WTSQuerySessionInformationA
 - WTSQuerySessionInformationW
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSQuerySessionInformationW function


## -description


Retrieves session information for the specified session on the specified Remote Desktop Session Host (RD Session Host) server. It can be used 
    to query session information on local and remote RD Session Host servers.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
      <a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> function, or specify 
      <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application 
      is running.


### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the session in which the calling application is running 
      (or the current session) specify <b>WTS_CURRENT_SESSION</b>. Only specify 
      <b>WTS_CURRENT_SESSION</b> when obtaining session information on the local server. If 
      <b>WTS_CURRENT_SESSION</b> is specified when querying session information on a remote server, 
      the returned session information will be inconsistent. Do not use the returned data.

You can use the <a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a> 
       function to retrieve the identifiers of all sessions on a specified RD Session Host server.

To query information for another user's session, you must have Query Information permission. For more 
       information, see <a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services 
       Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative 
       tool.


### -param WTSInfoClass [in]

A value of the <a href="https://msdn.microsoft.com/20e015bd-323a-44c4-a0d6-02781f3a5eec">WTS_INFO_CLASS</a> enumeration that indicates the type of 
    session information to retrieve in a call to the 
    <b>WTSQuerySessionInformation</b> function.


### -param ppBuffer [out]

A pointer to a variable that receives a pointer to the requested information. The format and contents of the 
      data depend on the information class specified in the <i>WTSInfoClass</i> parameter. To free 
      the returned buffer, call the <a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a> 
      function.


### -param pBytesReturned [out]

A pointer to a variable that receives the size, in bytes, of the data returned in 
      <i>ppBuffer</i>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To retrieve the session ID for the current session when Remote Desktop Services is running, call 
    <b>WTSQuerySessionInformation</b> and specify 
    <b>WTS_CURRENT_SESSION</b> for the <i>SessionId</i> parameter and 
    <b>WTSSessionId</b> for the <i>WTSInfoClass</i> parameter. The session ID 
    will be returned in the <i>ppBuffer</i> parameter. If Remote Desktop Services is not running, calls 
    to <b>WTSQuerySessionInformation</b> fail. In 
    this situation, you can retrieve the current session ID by calling the 
    <a href="https://msdn.microsoft.com/99a3f047-705c-40bc-8cc2-055257a4f2b3">ProcessIdToSessionId</a> function.

To determine whether your application is running on the physical console, you must specify 
    <b>WTS_CURRENT_SESSION</b> for the <i>SessionId</i> parameter, and 
    <b>WTSClientProtocolType</b> as the <i>WTSInfoClass</i> parameter. 
    If <i>ppBuffer</i> is "0", the session is attached to the physical console.




## -see-also




<a href="https://msdn.microsoft.com/11561aee-0b73-4e4a-8a53-11a46c7838c7">WTSCONFIGINFO</a>



<a href="https://msdn.microsoft.com/94aa2db0-d7e3-4ff2-bff0-d80983d2e8b2">WTSINFOEX</a>



<a href="https://msdn.microsoft.com/29034986-f8d1-4cf0-9f53-e4b195d450a6">WTS_CLIENT_ADDRESS</a>



<a href="https://msdn.microsoft.com/0d5e0a9d-23b0-4302-ade3-eb9fbd7f787d">WTS_CLIENT_DISPLAY</a>



<a href="https://msdn.microsoft.com/ee376f5a-3474-4e31-94c1-e760346eb794">WTS_CONNECTSTATE_CLASS</a>



<a href="https://msdn.microsoft.com/20e015bd-323a-44c4-a0d6-02781f3a5eec">WTS_INFO_CLASS</a>



<a href="https://msdn.microsoft.com/4a8846a3-2bad-4ea1-b614-aca18484ea86">WTS_SESSION_ADDRESS</a>
 

 

