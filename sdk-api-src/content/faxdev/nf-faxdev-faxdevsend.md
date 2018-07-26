---
UID: NF:faxdev.FaxDevSend
title: FaxDevSend function
author: windows-sdk-content
description: The fax service calls the FaxDevSend function to signal a fax service provider (FSP) that it must initiate an outgoing fax transmission. Each FSP must export the FaxDevSend function.
old-location: fax\_mfax_faxdevsend.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_7rz8.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxDevSend, FaxDevSend function [Fax Service], _mfax_faxdevsend, fax._mfax_faxdevsend, faxdev/FaxDevSend
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: faxdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevSend
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FaxDevSend function


## -description


The fax service calls the <b>FaxDevSend</b> function to signal a fax service provider (FSP) that it must initiate an outgoing fax transmission. Each FSP must export the <b>FaxDevSend</b> function.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a> function.


### -param FaxSend [in]

Type: <b>PFAX_SEND</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms684547(v=VS.85).aspx">FAX_SEND</a> structure that contains the sending information. For more information, see the following Remarks section.


### -param FaxSendCallback

Type: <b>PFAX_SEND_CALLBACK</b>

Pointer to a callback function that notifies the fax service of the call handle that TAPI assigns. For more information, see the following Remarks section.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  For a successful send, FaxDevSend() should return <b>TRUE</b> and FaxDevReportStatus() should return FS_COMPLETED. For an unsuccessful send, FaxDevSend() should return <b>FALSE</b>, and FaxDevReportStatus() should return any of the following codes: FS_LINE_UNAVAILABLE, FS_NO_ANSWER, FS_NO_DIAL_TONE, FS_DISCONNECTED, FS_BUSY, FS_NOT_FAX_CALL, or FS_FATAL_ERROR. If after a failed fax the fax should not be re-sent, FaxDevReportStatus() should return any code other than those listed here.</div>
<div> </div>



## -remarks




        The FSP must respond to the <b>FaxDevSend</b> function by making the call, sending the data, and terminating the call. The provider can call the <a href="https://msdn.microsoft.com/4a0e3fd7-9483-4d21-9b6f-bb6c04aa8226">lineSetMediaMode</a> function to correctly set the call's media mode. The fax service provider must dial the number specified by the <b>ReceiverNumber</b> member of the <a href="https://msdn.microsoft.com/library/ms684547(v=VS.85).aspx">FAX_SEND</a> structure. 
        


        The FSP has ownership of the line while in the context of the <b>FaxDevSend</b> function, and it must handle all protocol and error correction. 
        


        The data stream stored in the file specified by the <b>FileName</b> member of the <a href="https://msdn.microsoft.com/library/ms684547(v=VS.85).aspx">FAX_SEND</a> structure is a Tagged Image File Format Class F (TIFF Class F) file. For more information, see <a href="https://msdn.microsoft.com/library/ms693440(v=VS.85).aspx">Fax Image Format</a>. 
        


        To notify the fax service that a call has been established, the FSP must call the <a href="https://msdn.microsoft.com/library/ms684549(v=VS.85).aspx">FaxSendCallback</a> function pointed to by the <i>FaxSendCallback</i> parameter. The callback function also provides the fax service with the call handle that TAPI assigns. This handle is necessary for TAPI message routing. If the FSP does not call <i>FaxSendCallback</i>, it will miss all call-specific events for the send operation. 
        




## -see-also




<a href="https://msdn.microsoft.com/library/ms684547(v=VS.85).aspx">FAX_SEND</a>



<a href="https://msdn.microsoft.com/library/ms684546(v=VS.85).aspx">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/library/ms684535(v=VS.85).aspx">FaxDevReceive</a>



<a href="https://msdn.microsoft.com/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/library/ms684549(v=VS.85).aspx">FaxSendCallback</a>



<a href="https://msdn.microsoft.com/library/ms693428(v=VS.85).aspx">Using the Fax Service Provider API</a>
 

 

