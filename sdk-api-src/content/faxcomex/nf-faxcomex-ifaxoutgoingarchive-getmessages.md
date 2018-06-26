---
UID: NF:faxcomex.IFaxOutgoingArchive.GetMessages
title: IFaxOutgoingArchive::GetMessages
author: windows-sdk-content
description: The GetMessages method returns a new iterator (archive cursor) for the archive of outbound fax messages. For more information, see FaxOutgoingMessageIterator.
old-location: fax\_mfax_faxoutgoingarchive_getmessages.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_20qb.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxOutgoingArchive object [Fax Service],GetMessages method, FaxOutgoingArchive.GetMessages, GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],FaxOutgoingArchive object, IFaxOutgoingArchive.GetMessages, IFaxOutgoingArchive::GetMessages, _mfax_faxoutgoingarchive.getmessages, fax._mfax_faxoutgoingarchive_getmessages
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
 - FaxOutgoingArchive.GetMessages
 - IFaxOutgoingArchive.GetMessages
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingArchive::GetMessages


## -description


The <b>GetMessages</b> method returns a new iterator (archive cursor) for the archive of outbound fax messages. For more information, see <a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a>.


## -parameters




### -param lPrefetchSize

Type: <b>Long</b>

A <b>Long</b> value that specifies the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="https://msdn.microsoft.com/447a730c-6033-46ab-9d90-0aad1aa4a429">lDEFAULT_PREFETCH_SIZE</a>.


### -param pFaxOutgoingMessageIterator






#### - FaxOutgoingMessageIterator

Type: <b><a href="https://msdn.microsoft.com/5a34e012-33ae-4950-9f10-a3ad94142ef1">IFaxOutgoingMessageIterator</a>**</b>

A <a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a> object.


## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> or <b>farQUERY_OUT_ARCHIVE</b> access right. With the <b>farSUBMIT_LOW</b> access right, the user will be able to use this method only for his own faxes. With the <b>farQUERY_OUT_ARCHIVE</b> access right, he will be able to use this method for all of the faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/072eb2cc-7fd9-4f8e-8583-44384357e708">Visual Basic Example</a>
 

 

