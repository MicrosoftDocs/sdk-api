---
UID: NF:fxsutility.SendToFaxRecipient
title: SendToFaxRecipient function
author: windows-sdk-content
description: Called by an application to fax a file.
old-location: fax\_mfax_sendtofaxrecipient.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\shellextension\f\faxshell_sendtofaxrecipient.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SendToFaxRecipient, SendToFaxRecipient function [Fax Service], _mfax_sendtofaxrecipient, fax._mfax_sendtofaxrecipient, fxsutility/SendToFaxRecipient
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fxsutility.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Fxsutility.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fxsutility.dll
api_name:
 - SendToFaxRecipient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SendToFaxRecipient function


## -description


Called by an application to fax a file. 


## -parameters




### -param sndMode

Type: <b><a href="https://msdn.microsoft.com/6b9e75b2-1a79-4056-b3c8-215cb3e975b1">SendToMode</a></b>

A value specifying how to send the fax. For Windows Vista, this must be <a href="https://msdn.microsoft.com/6b9e75b2-1a79-4056-b3c8-215cb3e975b1">SEND_TO_FAX_RECIPIENT_ATTACHMENT</a>.


### -param lpFileName

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated string representing the name of the file to fax. 


## -returns



Type: <b>DWORD</b>

Zero, if the operation is successful.




## -remarks



Call <a href="https://msdn.microsoft.com/88f74423-f9dd-4846-a53a-a24ff08048d3">CanSendToFaxRecipient</a> first to determine if faxing from within an application is possible on the computer.  
        




## -see-also




<a href="https://msdn.microsoft.com/88f74423-f9dd-4846-a53a-a24ff08048d3">CanSendToFaxRecipient</a>



<a href="https://msdn.microsoft.com/6b9e75b2-1a79-4056-b3c8-215cb3e975b1">SendToMode</a>



<a href="https://msdn.microsoft.com/555ee494-ee1c-4047-b7ae-a890176a6b32">Shell Fax Extension Functions</a>
 

 

