---
UID: NF:wtsapi32.WTSSendMessageA
title: WTSSendMessageA function
author: windows-sdk-content
description: Displays a message box on the client desktop of a specified Remote Desktop Services session.
old-location: termserv\wtssendmessage.htm
old-project: termserv
ms.assetid: 4c70bc93-00b1-46ed-947d-b3cf61a5aca4
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IDABORT, IDASYNC, IDCANCEL, IDCONTINUE, IDIGNORE, IDNO, IDOK, IDRETRY, IDTIMEOUT, IDTRYAGAIN, IDYES, WTSSendMessage, WTSSendMessage function [Remote Desktop Services], WTSSendMessageA, WTSSendMessageW, _win32_wtssendmessage, termserv.wtssendmessage, wtsapi32/WTSSendMessage, wtsapi32/WTSSendMessageA, wtsapi32/WTSSendMessageW
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
req.unicode-ansi: WTSSendMessageW (Unicode) and WTSSendMessageA (ANSI)
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
api_name:
 - WTSSendMessage
 - WTSSendMessageA
 - WTSSendMessageW
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSSendMessageA function


## -description


Displays a message box on the client desktop of a 
    specified Remote Desktop Services session.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
      <a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> function, or specify 
       <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application 
       is running.


### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify 
      <b>WTS_CURRENT_SESSION</b>. You can use the 
      <a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a> function to retrieve 
      the identifiers of all sessions on a specified RD Session Host server.

To send a message to another user's session, you need to have the Message permission. For more 
       information, see <a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services  
       Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative 
       tool.


### -param pTitle [in]

A pointer to a null-terminated string for the title bar of the message box.


### -param TitleLength [in]

The length, in bytes, of the title bar string.


### -param pMessage [in]

A pointer to a null-terminated string that contains the message to display.


### -param MessageLength [in]

The length, in bytes, of the message string.


### -param Style [in]

The contents and behavior of the message box. This value is typically 
      <b>MB_OK</b>. For a complete list of values, see the <i>uType</i> 
      parameter of the <a href="winui._win32_messagebox">MessageBox</a> function.


### -param Timeout [in]

The time, in seconds, that the <b>WTSSendMessage</b> function waits for 
      the user's response. If the user does not respond within the time-out interval, the 
      <i>pResponse</i> parameter returns <b>IDTIMEOUT</b>. If the 
      <i>Timeout</i> parameter is zero, <b>WTSSendMessage</b> waits 
      indefinitely for the user to respond.


### -param pResponse [out]

A pointer to a variable that receives the user's response, which can be one of the following values.



#### IDABORT (3)

<b>Abort</b>



#### IDCANCEL (2)

<b>Cancel</b>



#### IDCONTINUE (11)

<b>Continue</b>



#### IDIGNORE (5)

<b>Ignore</b>



#### IDNO (7)

<b>No</b>



#### IDOK (1)

<b>OK</b>



#### IDRETRY (4)

<b>Retry</b>



#### IDTRYAGAIN (10)

<b>Try Again</b>



#### IDYES (6)

<b>Yes</b>



#### IDASYNC (32001 (0x7D01))

The <i>bWait</i> parameter was <b>FALSE</b>, so the function 
        returned without waiting for a response.



#### IDTIMEOUT (32000 (0x7D00))

The <i>bWait</i> parameter was <b>TRUE</b> and the time-out 
        interval elapsed.


### -param bWait [in]

If <b>TRUE</b>, <b>WTSSendMessage</b> does not return until 
      the user responds or the time-out interval elapses. If the <i>Timeout</i> parameter is zero, 
      the function does not return until the user responds.

If <b>FALSE</b>, the function returns immediately and the 
       <i>pResponse</i> parameter returns <b>IDASYNC</b>. Use this method for 
       simple information messages (such as print job–notification messages) that do not need to return the 
       user's response to the calling program.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="winui._win32_messagebox">MessageBox</a>
 

 

