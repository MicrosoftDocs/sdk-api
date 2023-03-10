---
UID: NF:faxcomex.IFaxRecipient.put_FaxNumber
title: IFaxRecipient::put_FaxNumber (faxcomex.h)
description: The IFaxRecipient::get_FaxNumber property is a null-terminated string that contains the fax number associated with the recipient. (Put)
helpviewer_keywords: ["FaxNumber property [Fax Service]","FaxNumber property [Fax Service]","IFaxRecipient interface","IFaxRecipient interface [Fax Service]","FaxNumber property","IFaxRecipient.FaxNumber","IFaxRecipient.get_FaxNumber","IFaxRecipient.put_FaxNumber","IFaxRecipient::FaxNumber","IFaxRecipient::get_FaxNumber","IFaxRecipient::put_FaxNumber","_mfax_faxrecipient.faxnumber","fax._mfax_faxrecipient_cpp_mfax_faxrecipient_faxnumber_cpp","fax._mfax_faxrecipient_faxnumber","faxcomex/IFaxRecipient::FaxNumber","faxcomex/IFaxRecipient::get_FaxNumber","faxcomex/IFaxRecipient::put_FaxNumber","put_FaxNumber"]
old-location: fax\_mfax_faxrecipient_cpp_mfax_faxrecipient_faxnumber_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_284y.htm
ms.date: 12/05/2018
ms.keywords: FaxNumber property [Fax Service], FaxNumber property [Fax Service],IFaxRecipient interface, IFaxRecipient interface [Fax Service],FaxNumber property, IFaxRecipient.FaxNumber, IFaxRecipient.get_FaxNumber, IFaxRecipient.put_FaxNumber, IFaxRecipient::FaxNumber, IFaxRecipient::get_FaxNumber, IFaxRecipient::put_FaxNumber, _mfax_faxrecipient.faxnumber, fax._mfax_faxrecipient_cpp_mfax_faxrecipient_faxnumber_cpp, fax._mfax_faxrecipient_faxnumber, faxcomex/IFaxRecipient::FaxNumber, faxcomex/IFaxRecipient::get_FaxNumber, faxcomex/IFaxRecipient::put_FaxNumber, put_FaxNumber
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
 - IFaxRecipient::put_FaxNumber
 - faxcomex/IFaxRecipient::put_FaxNumber
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
 - IFaxRecipient.FaxNumber
 - IFaxRecipient.get_FaxNumber
 - IFaxRecipient.put_FaxNumber
 - IFaxRecipient.get_FaxNumber
 - IFaxRecipient.put_FaxNumber
---

# IFaxRecipient::put_FaxNumber


## -description

The <b>IFaxRecipient::get_FaxNumber</b> property is a null-terminated string that contains the fax number associated with the recipient.



This property is read/write.

## -parameters

## -remarks

If this string contains a canonical fax number (defined in the <a href="/windows/desktop/Tapi/address-ovr">Address</a> topic of the Telephony Application Programming Interface (TAPI) documentation—see the <i>Canonical Addresses</i> subheading), then the outbound routing rules will be applied. Otherwise, the first available device will be used and the fax number we be dialed as it appears in the string.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-broadcasting-a-fax">Broadcasting a Fax</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxrecipient">FaxRecipient</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxrecipient">IFaxRecipient</a>
