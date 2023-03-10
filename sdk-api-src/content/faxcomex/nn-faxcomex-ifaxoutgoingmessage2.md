---
UID: NN:faxcomex.IFaxOutgoingMessage2
title: IFaxOutgoingMessage2 (faxcomex.h)
description: Used by a fax client application to retrieve information about a sent fax message in the archive of outbound faxes.
helpviewer_keywords: ["IFaxOutgoingMessage2","IFaxOutgoingMessage2 interface [Fax Service]","IFaxOutgoingMessage2 interface [Fax Service]","described","_mfax_faxoutgoingmessage2_cpp","fax._mfax_faxoutgoingmessage2_cpp","faxcomex/IFaxOutgoingMessage2"]
old-location: fax\_mfax_faxoutgoingmessage2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\faxinta_n_ifaxoutgoingmessage2_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessage2, IFaxOutgoingMessage2 interface [Fax Service], IFaxOutgoingMessage2 interface [Fax Service],described, _mfax_faxoutgoingmessage2_cpp, fax._mfax_faxoutgoingmessage2_cpp, faxcomex/IFaxOutgoingMessage2
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
 - IFaxOutgoingMessage2
 - faxcomex/IFaxOutgoingMessage2
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
 - IFaxOutgoingMessage2
---

# IFaxOutgoingMessage2 interface


## -description

Used by a fax client application to retrieve information about a sent fax message in the archive of outbound faxes. The archive contains faxes sent successfully by the fax service. The interface inherits all the functionality of the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a> interface. It adds to that information such as whether the fax has a cover page, whether it has been read and what kind of receipt was sent.

The <b>IFaxOutgoingMessage2</b> interface is accessed through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a> interface or <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a> interface.


<div class="alert"><b>Note</b>  This interface is supported only on Windows Vista or later.</div><div> </div>

## -inheritance

The <b>IFaxOutgoingMessage2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>. <b>IFaxOutgoingMessage2</b> also has these types of members:

## -remarks

To create a <b>FaxIncomingMessage2</b> object in C++, call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingarchive-getmessage-vb">IFaxAccountOutgoingArchive::GetMessage</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-message">Message</a> method.

A default implementation of this interface is provided by the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> object in Windows Vista or later. The <b>FaxOutgoingMessage</b> object implements the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a> interface on Windows XP or earlier.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>
