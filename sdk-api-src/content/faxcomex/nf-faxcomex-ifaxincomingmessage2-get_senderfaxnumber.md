---
UID: NF:faxcomex.IFaxIncomingMessage2.get_SenderFaxNumber
title: IFaxIncomingMessage2::get_SenderFaxNumber (faxcomex.h)
description: Contains the sender's fax number associated with the inbound fax message. This property is a null-terminated string. (Get)
helpviewer_keywords: ["IFaxIncomingMessage2 interface [Fax Service]","SenderFaxNumber property","IFaxIncomingMessage2.SenderFaxNumber","IFaxIncomingMessage2.get_SenderFaxNumber","IFaxIncomingMessage2.put_SenderFaxNumber","IFaxIncomingMessage2::SenderFaxNumber","IFaxIncomingMessage2::get_SenderFaxNumber","IFaxIncomingMessage2::put_SenderFaxNumber","SenderFaxNumber property [Fax Service]","SenderFaxNumber property [Fax Service]","IFaxIncomingMessage2 interface","_mfax_faxincomingmessage.senderfaxnumber","fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_senderfaxnumber_cpp","fax._mfax_faxincomingmessage_senderfaxnumber","faxcomex/IFaxIncomingMessage2::SenderFaxNumber","faxcomex/IFaxIncomingMessage2::get_SenderFaxNumber","faxcomex/IFaxIncomingMessage2::put_SenderFaxNumber","get_SenderFaxNumber"]
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_senderfaxnumber_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\senderfaxnumber.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],SenderFaxNumber property, IFaxIncomingMessage2.SenderFaxNumber, IFaxIncomingMessage2.get_SenderFaxNumber, IFaxIncomingMessage2.put_SenderFaxNumber, IFaxIncomingMessage2::SenderFaxNumber, IFaxIncomingMessage2::get_SenderFaxNumber, IFaxIncomingMessage2::put_SenderFaxNumber, SenderFaxNumber property [Fax Service], SenderFaxNumber property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.senderfaxnumber, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_senderfaxnumber_cpp, fax._mfax_faxincomingmessage_senderfaxnumber, faxcomex/IFaxIncomingMessage2::SenderFaxNumber, faxcomex/IFaxIncomingMessage2::get_SenderFaxNumber, faxcomex/IFaxIncomingMessage2::put_SenderFaxNumber, get_SenderFaxNumber
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxIncomingMessage2::get_SenderFaxNumber
 - faxcomex/IFaxIncomingMessage2::get_SenderFaxNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingMessage2.SenderFaxNumber
 - IFaxIncomingMessage2.get_SenderFaxNumber
 - IFaxIncomingMessage2.put_SenderFaxNumber
 - IFaxIncomingMessage2.get_SenderFaxNumber
 - IFaxIncomingMessage2.put_SenderFaxNumber
---

# IFaxIncomingMessage2::get_SenderFaxNumber


## -description

Contains the sender's fax number associated with the inbound fax message. This property is a null-terminated string. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.

## -parameters

## -remarks

A received message starts with a null value for the sender's fax number when it arrives. A <a href="/previous-versions/windows/desktop/fax/-mfax-glossary">routing assistant</a> can specify the sender's fax number when the fax is reassigned.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage2">IFaxIncomingMessage2</a>
