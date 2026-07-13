---
UID: NF:faxcomex.IFaxIncomingMessage2.get_HasCoverPage
title: IFaxIncomingMessage2::get_HasCoverPage (faxcomex.h)
description: A flag that indicates whether the fax has a cover page. (Get)
helpviewer_keywords: ["HasCoverPage property [Fax Service]","HasCoverPage property [Fax Service]","IFaxIncomingMessage2 interface","IFaxIncomingMessage2 interface [Fax Service]","HasCoverPage property","IFaxIncomingMessage2.HasCoverPage","IFaxIncomingMessage2.get_HasCoverPage","IFaxIncomingMessage2.put_HasCoverPage","IFaxIncomingMessage2::HasCoverPage","IFaxIncomingMessage2::get_HasCoverPage","IFaxIncomingMessage2::put_HasCoverPage","_mfax_faxincomingmessage.hascoverpage","fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_hascoverpage_cpp","fax._mfax_faxincomingmessage_hascoverpage","faxcomex/IFaxIncomingMessage2::HasCoverPage","faxcomex/IFaxIncomingMessage2::get_HasCoverPage","faxcomex/IFaxIncomingMessage2::put_HasCoverPage","get_HasCoverPage"]
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_hascoverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\hascoverpage.htm
ms.date: 12/05/2018
ms.keywords: HasCoverPage property [Fax Service], HasCoverPage property [Fax Service],IFaxIncomingMessage2 interface, IFaxIncomingMessage2 interface [Fax Service],HasCoverPage property, IFaxIncomingMessage2.HasCoverPage, IFaxIncomingMessage2.get_HasCoverPage, IFaxIncomingMessage2.put_HasCoverPage, IFaxIncomingMessage2::HasCoverPage, IFaxIncomingMessage2::get_HasCoverPage, IFaxIncomingMessage2::put_HasCoverPage, _mfax_faxincomingmessage.hascoverpage, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_hascoverpage_cpp, fax._mfax_faxincomingmessage_hascoverpage, faxcomex/IFaxIncomingMessage2::HasCoverPage, faxcomex/IFaxIncomingMessage2::get_HasCoverPage, faxcomex/IFaxIncomingMessage2::put_HasCoverPage, get_HasCoverPage
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
 - IFaxIncomingMessage2::get_HasCoverPage
 - faxcomex/IFaxIncomingMessage2::get_HasCoverPage
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
 - IFaxIncomingMessage2.HasCoverPage
 - IFaxIncomingMessage2.get_HasCoverPage
 - IFaxIncomingMessage2.put_HasCoverPage
 - IFaxIncomingMessage2.get_HasCoverPage
 - IFaxIncomingMessage2.put_HasCoverPage
---

# IFaxIncomingMessage2::get_HasCoverPage


## -description

A flag that indicates whether the fax has a cover page. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.

## -parameters

## -remarks

A received message has a VARIANT_FALSE value when it arrives. A <a href="/previous-versions/windows/desktop/fax/-mfax-glossary">routing assistant</a> application can set this to VARIANT_TRUE when it is reassigned. 

A change to this value is not committed to the server until <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-save-vb">IFaxIncomingMessage2::Save</a> is called.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage2">IFaxIncomingMessage2</a>
