---
UID: NF:faxcomex.IFaxIncomingMessage2.get_Subject
title: IFaxIncomingMessage2::get_Subject (faxcomex.h)
description: The Subject property contains the subject associated with the inbound fax message. This property is a null-terminated string. (Get)
helpviewer_keywords: ["IFaxIncomingMessage2 interface [Fax Service]","Subject property","IFaxIncomingMessage2.Subject","IFaxIncomingMessage2.get_Subject","IFaxIncomingMessage2.put_Subject","IFaxIncomingMessage2::Subject","IFaxIncomingMessage2::get_Subject","IFaxIncomingMessage2::put_Subject","Subject property [Fax Service]","Subject property [Fax Service]","IFaxIncomingMessage2 interface","_mfax_faxincomingmessage.subject","fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_subject_cpp","fax._mfax_faxincomingmessage_subject","faxcomex/IFaxIncomingMessage2::Subject","faxcomex/IFaxIncomingMessage2::get_Subject","faxcomex/IFaxIncomingMessage2::put_Subject","get_Subject"]
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_subject_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\subject.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Subject property, IFaxIncomingMessage2.Subject, IFaxIncomingMessage2.get_Subject, IFaxIncomingMessage2.put_Subject, IFaxIncomingMessage2::Subject, IFaxIncomingMessage2::get_Subject, IFaxIncomingMessage2::put_Subject, Subject property [Fax Service], Subject property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.subject, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_subject_cpp, fax._mfax_faxincomingmessage_subject, faxcomex/IFaxIncomingMessage2::Subject, faxcomex/IFaxIncomingMessage2::get_Subject, faxcomex/IFaxIncomingMessage2::put_Subject, get_Subject
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
 - IFaxIncomingMessage2::get_Subject
 - faxcomex/IFaxIncomingMessage2::get_Subject
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
 - IFaxIncomingMessage2.Subject
 - IFaxIncomingMessage2.get_Subject
 - IFaxIncomingMessage2.put_Subject
 - IFaxIncomingMessage2.get_Subject
 - IFaxIncomingMessage2.put_Subject
---

# IFaxIncomingMessage2::get_Subject


## -description

The <b>Subject</b> property contains the subject associated with the inbound fax message. This property is a null-terminated string.


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.

## -parameters

## -remarks

A received message starts with a null value for the subject when it arrives. It can be given a subject by a <a href="/previous-versions/windows/desktop/fax/-mfax-glossary">routing assistant</a> when it is reassigned.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage2">IFaxIncomingMessage2</a>
