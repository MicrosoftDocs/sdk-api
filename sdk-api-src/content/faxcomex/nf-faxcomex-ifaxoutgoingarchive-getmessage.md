---
UID: NF:faxcomex.IFaxOutgoingArchive.GetMessage
title: IFaxOutgoingArchive::GetMessage
author: windows-sdk-content
description: The GetMessage method returns a fax message from the archive of outbound faxes by using the fax message ID.
old-location: fax\_mfax_faxoutgoingarchive_getmessage.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7did.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxOutgoingArchive object [Fax Service],GetMessage method, FaxOutgoingArchive.GetMessage, GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],FaxOutgoingArchive object, IFaxOutgoingArchive.GetMessage, IFaxOutgoingArchive::GetMessage, _mfax_faxoutgoingarchive.getmessage, fax._mfax_faxoutgoingarchive_getmessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutgoingArchive.GetMessage
 - IFaxOutgoingArchive.GetMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingArchive::GetMessage


## -description


The <b>GetMessage</b> method returns a fax message from the archive of outbound faxes by using the fax message ID.


## -parameters




### -param bstrMessageId

Type: <b>String</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of outbound faxes.


### -param pFaxOutgoingMessage






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a></b>

A <a href="https://msdn.microsoft.com/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a> object.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <b>farQUERY_OUT_ARCHIVE</b> access right. With the <b>farSUBMIT_LOW</b> access right, the user will be able to use this method only for his own faxes. With the <b>farQUERY_OUT_ARCHIVE</b> access right, he will be able to use this method for all of the faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/library/ms688636(v=VS.85).aspx">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/library/ms693472(v=VS.85).aspx">Visual Basic Example</a>
 

 

