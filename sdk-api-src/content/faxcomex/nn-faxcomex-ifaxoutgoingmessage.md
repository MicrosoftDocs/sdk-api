---
UID: NN:faxcomex.IFaxOutgoingMessage
title: IFaxOutgoingMessage (faxcomex.h)
description: The IFaxOutgoingMessage interface describes an object that is used by a fax client application to retrieve information about a fax message in the archive of outbound faxes.
helpviewer_keywords: ["IFaxOutgoingMessage","IFaxOutgoingMessage interface [Fax Service]","IFaxOutgoingMessage interface [Fax Service]","described","_mfax_faxoutgoingmessage_cpp","fax._mfax_faxoutgoingmessage_cpp","faxcomex/IFaxOutgoingMessage"]
old-location: fax\_mfax_faxoutgoingmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8ujp_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessage, IFaxOutgoingMessage interface [Fax Service], IFaxOutgoingMessage interface [Fax Service],described, _mfax_faxoutgoingmessage_cpp, fax._mfax_faxoutgoingmessage_cpp, faxcomex/IFaxOutgoingMessage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutgoingMessage
 - faxcomex/IFaxOutgoingMessage
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
 - IFaxOutgoingMessage
---

# IFaxOutgoingMessage interface


## -description

The <b>IFaxOutgoingMessage</b> interface describes an object that is used by a fax client application to retrieve information about a fax message in the archive of outbound faxes. The archive contains faxes transmitted successfully by the fax service. The object enables you to retrieve information about the fax recipient, contained in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxrecipient">FaxRecipient</a> object, and information about the fax sender, contained in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a> object. It also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message, to a file on the local computer.

## -inheritance

The <b>IFaxOutgoingMessage</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutgoingMessage</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxOutgoingMessage</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> object.
