---
UID: NF:faxcomex.IFaxIncomingMessage2.put_Read
title: IFaxIncomingMessage2::put_Read (faxcomex.h)
description: A flag that indicates if the fax has been read. (Put)
helpviewer_keywords: ["IFaxIncomingMessage2 interface [Fax Service]","Read property","IFaxIncomingMessage2.Read","IFaxIncomingMessage2.get_Read","IFaxIncomingMessage2.put_Read","IFaxIncomingMessage2::Read","IFaxIncomingMessage2::get_Read","IFaxIncomingMessage2::put_Read","Read property [Fax Service]","Read property [Fax Service]","IFaxIncomingMessage2 interface","_mfax_faxincomingmessage.read","fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_read_cpp","fax._mfax_faxincomingmessage_read","faxcomex/IFaxIncomingMessage2::Read","faxcomex/IFaxIncomingMessage2::get_Read","faxcomex/IFaxIncomingMessage2::put_Read","put_Read"]
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_read_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\read.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Read property, IFaxIncomingMessage2.Read, IFaxIncomingMessage2.get_Read, IFaxIncomingMessage2.put_Read, IFaxIncomingMessage2::Read, IFaxIncomingMessage2::get_Read, IFaxIncomingMessage2::put_Read, Read property [Fax Service], Read property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.read, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_read_cpp, fax._mfax_faxincomingmessage_read, faxcomex/IFaxIncomingMessage2::Read, faxcomex/IFaxIncomingMessage2::get_Read, faxcomex/IFaxIncomingMessage2::put_Read, put_Read
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
 - IFaxIncomingMessage2::put_Read
 - faxcomex/IFaxIncomingMessage2::put_Read
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
 - IFaxIncomingMessage2.Read
 - IFaxIncomingMessage2.get_Read
 - IFaxIncomingMessage2.put_Read
 - IFaxIncomingMessage2.get_Read
 - IFaxIncomingMessage2.put_Read
---

# IFaxIncomingMessage2::put_Read


## -description

A flag that indicates if the fax has been read. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.

## -parameters

## -remarks

Possible values are VARIANT_TRUE and VARIANT_FALSE.

A change to this value is not committed to the server until <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-save-vb">IFaxIncomingMessage2::Save</a> is called.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage2">IFaxIncomingMessage2</a>
