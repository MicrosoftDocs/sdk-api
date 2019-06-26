---
UID: NF:fxsutility.SendToFaxRecipient
title: SendToFaxRecipient function (fxsutility.h)
author: windows-sdk-content
description: Called by an application to fax a file.
old-location: fax\_mfax_sendtofaxrecipient.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\shellextension\f\faxshell_sendtofaxrecipient.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SendToFaxRecipient, SendToFaxRecipient function [Fax Service], _mfax_sendtofaxrecipient, fax._mfax_sendtofaxrecipient, fxsutility/SendToFaxRecipient
ms.topic: function
f1_keywords: 
 - "fxsutility/SendToFaxRecipient"
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
ms.custom: 19H1
---

# SendToFaxRecipient function


## -description


Called by an application to fax a file. 


## -parameters




### -param sndMode

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fxsutility/ne-fxsutility-sendtomode">SendToMode</a></b>

A value specifying how to send the fax. For Windows Vista, this must be <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fxsutility/ne-fxsutility-sendtomode">SEND_TO_FAX_RECIPIENT_ATTACHMENT</a>.


### -param lpFileName

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated string representing the name of the file to fax. 


## -returns



Type: <b>DWORD</b>

Zero, if the operation is successful.




## -remarks



Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fxsutility/nf-fxsutility-cansendtofaxrecipient">CanSendToFaxRecipient</a> first to determine if faxing from within an application is possible on the computer.  
        




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fxsutility/nf-fxsutility-cansendtofaxrecipient">CanSendToFaxRecipient</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fxsutility/ne-fxsutility-sendtomode">SendToMode</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-shell-fax-extension-functions">Shell Fax Extension Functions</a>
 

 

