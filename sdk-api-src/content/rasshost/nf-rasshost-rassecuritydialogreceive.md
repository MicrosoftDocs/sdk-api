---
UID: NF:rasshost.RasSecurityDialogReceive
title: RasSecurityDialogReceive function
author: windows-driver-content
description: The RasSecurityDialogReceive function starts an asynchronous operation that receives a remote user's response to a security challenge.
old-location: rras\rassecuritydialogreceive.htm
old-project: RRAS
ms.assetid: ed5fcea6-6533-4c78-bd49-dfeaafd8192a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: RasSecurityDialogReceive, RasSecurityDialogReceive function [RAS], _ras_rassecuritydialogreceive, rasshost/RasSecurityDialogReceive, rras.rassecuritydialogreceive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rasshost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RAS_AUTH_ATTRIBUTE, *PRAS_AUTH_ATTRIBUTE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rasman.dll
api_name:
-	RasSecurityDialogReceive
product: Windows
targetos: Windows
req.lib: 
req.dll: Rasman.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RasSecurityDialogReceive function


## -description


The 
<b>RasSecurityDialogReceive</b> function starts an asynchronous operation that receives a remote user's response to a security challenge. The response is the input that the user typed in a terminal window on the remote computer. A third-party RAS security DLL calls this function as part of its authentication of the remote user.

To call this function, first call the 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function to load Rasman.dll. Then call the 
<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function to get the DLL's 
<b>RasSecurityDialogReceive</b> entry point.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters




### -param hPort [in]

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a> call for this authentication transaction.


### -param pBuffer [in]

Pointer to the receive buffer that was passed to the security DLL in the 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a> call. When the asynchronous receive operation has been completed successfully, this buffer specifies the response from the remote user.


### -param pBufferLength [in]

Pointer to a <b>WORD</b> variable. This variable must specify the size, in bytes, of the <i>pBuffer</i> buffer. When the receive operation has been completed, the variable indicates the number of bytes returned in the <i>pBuffer</i> buffer.


### -param Timeout [in]

Specifies a time-out period, in seconds, after which the RAS server sets the <i>hEvent</i> event object to the signaled state. 




If this value is zero, there is no time-out period; that is, the RAS server does not signal the event object until the receive operation has been completed.


### -param hEvent [in]

Specifies the handle of an event object created by the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function. The RAS server sets the event object to the signaled state when the receive operation has been completed or when the time-out period has elapsed.


## -returns



If the function is successful, the return value is PENDING (defined in Raserror.h). This indicates that the receive operation is in progress.

If an error occurs, the return value is one of the error codes defined in Raserror.h or Winerror.h. 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> does not provide extended error information.




## -remarks



After calling the 
<a href="https://msdn.microsoft.com/adbc357b-7a5d-426d-b21f-0b1478bb2348">RasSecurityDialogSend</a> function to send a security challenge to the remote user, the security DLL must call the 
<b>RasSecurityDialogReceive</b> function to get the user's response.

The 
<b>RasSecurityDialogReceive</b> function is asynchronous. When the function returns, the security DLL must use one of the wait functions, such as 
<a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a>, to wait for the <i>hEvent</i> event object to be signaled. The RAS server signals the event object when the receive operation has been completed or when the time-out interval has elapsed. If the receive operation is successful, the <i>pBuffer</i> buffer contains the response from the remote user, and the <i>pBufferLength</i> parameter indicates the number of bytes received. If the remote user sends more bytes than will fit in the buffer, the RAS server buffers the excess bytes and returns them in the next 
<b>RasSecurityDialogReceive</b> call.

Use the <i>Timeout</i> parameter to specify a time-out interval. If the time-out elapses, the RAS server signals the event object, and the <i>pBufferLength</i> parameter indicates that zero bytes were transferred. Alternatively, set <i>Timeout</i> to zero, and specify a time-out interval in the wait function used to wait for the event object.

When a security DLL is authenticating a remote user, the connection operation on the remote computer enters a RASCS_Interactive paused state. The message sent by 
<a href="https://msdn.microsoft.com/adbc357b-7a5d-426d-b21f-0b1478bb2348">RasSecurityDialogSend</a> is displayed as output in a terminal window on the remote computer. The response received by 
<b>RasSecurityDialogReceive</b> is the input that the remote user types in the terminal window. The RASCS_Interactive value is defined in the 
<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/44c000d7-2bb6-4fd8-ac5f-9d3850d857a0">RAS Server Administration Functions</a>



<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a>



<a href="https://msdn.microsoft.com/adbc357b-7a5d-426d-b21f-0b1478bb2348">RasSecurityDialogSend</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a>
 

 

