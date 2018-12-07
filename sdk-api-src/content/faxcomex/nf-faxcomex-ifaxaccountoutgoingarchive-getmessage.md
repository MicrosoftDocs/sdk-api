---
UID: NF:faxcomex.IFaxAccountOutgoingArchive.GetMessage
title: IFaxAccountOutgoingArchive::GetMessage
author: windows-sdk-content
description: Returns a fax message from the archive of outbound faxes for a particular fax account, by using the fax message ID.
old-location: fax\_mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingarchive\getmessage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxAccountOutgoingArchive interface, IFaxAccountOutgoingArchive interface [Fax Service],GetMessage method, IFaxAccountOutgoingArchive.GetMessage, IFaxAccountOutgoingArchive::GetMessage, _mfax_faxaccountoutgoingarchive.getmessage, fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessage_cpp, fax._mfax_faxaccountoutgoingarchive_getmessage, faxcomex/IFaxAccountOutgoingArchive::GetMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
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
 - IFaxAccountOutgoingArchive.GetMessage
 - IFaxAccountOutgoingArchive.GetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountOutgoingArchive::GetMessage


## -description


Returns a fax message from the archive of outbound faxes for a particular fax account, by using the fax message ID.


## -parameters




### -param bstrMessageId [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of outbound faxes.


### -param pFaxOutgoingMessage

TBD




#### - pFaxOutgoingMessage2 [out, retval]

Type: <b><a href="https://msdn.microsoft.com/c6468db0-ea8d-4460-b389-43608337bd96">IFaxOutgoingMessage2</a>**</b>

A <a href="https://msdn.microsoft.com/c6468db0-ea8d-4460-b389-43608337bd96">IFaxOutgoingMessage2</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/21ed0cc8-23a3-4ac1-853f-8f7d004cf843">FaxAccountOutgoingArchive</a>



<a href="https://msdn.microsoft.com/cd2441ba-ed29-4ba5-b3f7-804fbca4d421">IFaxAccountOutgoingArchive</a>
 

 

