---
UID: NF:rasshost.RasSecurityDialogSend
title: RasSecurityDialogSend function
author: windows-sdk-content
description: The RasSecurityDialogSend function sends a message to be displayed in a terminal window on a remote computer. A third-party RAS security DLL sends this message as part of its authentication of a remote user.
old-location: rras\rassecuritydialogsend.htm
tech.root: rras
ms.assetid: adbc357b-7a5d-426d-b21f-0b1478bb2348
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RasSecurityDialogSend, RasSecurityDialogSend function [RAS], _ras_rassecuritydialogsend, rasshost/RasSecurityDialogSend, rras.rassecuritydialogsend
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
req.lib: 
req.dll: Rasman.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasman.dll
api_name:
 - RasSecurityDialogSend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasSecurityDialogSend function


## -description


The 
<b>RasSecurityDialogSend</b> function sends a message to be displayed in a terminal window on a remote computer. A third-party RAS security DLL sends this message as part of its authentication of a remote user.

To call this function, first call the 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function to load Rasman.dll. Then call the 
<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function to get the DLL's 
<b>RasSecurityDialogSend</b> entry point.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters




### -param hPort [in]

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a> call for this authentication transaction.


### -param pBuffer [in]

Pointer to the send buffer that was passed to the security DLL in the call to 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a>. Before calling 
<b>RasSecurityDialogSend</b>, copy into this buffer the message to send to the remote user. The <i>SendBufSize</i> parameter of the 
<b>RasSecurityDialogBegin</b> function indicates the maximum number of bytes the buffer can store.


### -param BufferLength [in]

Specifies the number of bytes to send in the <i>pBuffer</i> buffer.


## -returns



If the function is successful, the return value is PENDING (defined in Raserror.h). This indicates that the send operation is in progress.

If an error occurs, the return value is one of the error codes defined in Raserror.h or Winerror.h. 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> does not provide extended error information.




## -remarks



The 
<b>RasSecurityDialogSend</b> function is asynchronous. After calling it to send a message to the remote user, call the 
<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a> function, and then wait for a response. The security DLL can make any number of 
<b>RasSecurityDialogSend</b> calls, with each call followed by a 
<b>RasSecurityDialogReceive</b> call.

When a security DLL is authenticating a remote user, the connection operation on the remote computer enters a RASCS_Interactive paused state. The message sent by 
<b>RasSecurityDialogSend</b> is displayed as output in a terminal window on the remote computer. The response received by 
<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a> is the input that the remote user types in the terminal window. The RASCS_Interactive value is defined in the 
<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/44c000d7-2bb6-4fd8-ac5f-9d3850d857a0">RAS Server Administration Functions</a>



<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a>



<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a>



<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>
 

 

