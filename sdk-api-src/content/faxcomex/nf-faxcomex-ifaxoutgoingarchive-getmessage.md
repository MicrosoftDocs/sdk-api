---
UID: NF:faxcomex.IFaxOutgoingArchive.GetMessage
title: IFaxOutgoingArchive::GetMessage
author: windows-sdk-content
description: The IFaxOutgoingArchive::GetMessage method returns a fax message from the archive of outbound faxes by using the fax message ID.
old-location: fax\_mfax_faxoutgoingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7did_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],GetMessage method, IFaxOutgoingArchive.GetMessage, IFaxOutgoingArchive::GetMessage, _mfax_faxoutgoingarchive.getmessage_cpp, fax._mfax_faxoutgoingarchive_getmessage_cpp, faxcomex/IFaxOutgoingArchive::GetMessage
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingArchive.GetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxOutgoingArchive.GetMessage
: 
---

# IFaxOutgoingArchive::GetMessage


## -description


The <b>IFaxOutgoingArchive::GetMessage</b> method returns a fax message from the archive of outbound faxes by using the fax message ID.


## -parameters




### -param bstrMessageId

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of outbound faxes.


### -param pFaxOutgoingMessage [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7423ccd1-5eb6-402f-99fb-2cbed386450a">IFaxOutgoingMessage</a>**</b>

Address of a pointer that receives a <a href="https://msdn.microsoft.com/7423ccd1-5eb6-402f-99fb-2cbed386450a">IFaxOutgoingMessage</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> or <b>farQUERY_OUT_ARCHIVE</b> access right. With the <b>farSUBMIT_LOW</b> access right, the user will be able to use this method only for his own faxes. With the <b>farQUERY_OUT_ARCHIVE</b> access right, he will be able to use this method for all of the faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/68f6c0f2-ea06-401c-9021-c50940f8cd7a">Visual Basic Example</a>
 

 

