---
UID: NF:faxcomex.IFaxAccountIncomingArchive.get_SizeLow
title: IFaxAccountIncomingArchive::get_SizeLow (faxcomex.h)
description: Specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.
helpviewer_keywords: ["IFaxAccountIncomingArchive interface [Fax Service]","SizeLow property","IFaxAccountIncomingArchive.SizeLow","IFaxAccountIncomingArchive.get_SizeLow","IFaxAccountIncomingArchive::SizeLow","IFaxAccountIncomingArchive::get_SizeLow","SizeLow property [Fax Service]","SizeLow property [Fax Service]","IFaxAccountIncomingArchive interface","_mfax_faxaccountincomingarchive.sizelow","fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizelow_cpp","fax._mfax_faxaccountincomingarchive_sizelow","faxcomex/IFaxAccountIncomingArchive::SizeLow","faxcomex/IFaxAccountIncomingArchive::get_SizeLow","get_SizeLow"]
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizelow_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\sizelow.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountIncomingArchive interface [Fax Service],SizeLow property, IFaxAccountIncomingArchive.SizeLow, IFaxAccountIncomingArchive.get_SizeLow, IFaxAccountIncomingArchive::SizeLow, IFaxAccountIncomingArchive::get_SizeLow, SizeLow property [Fax Service], SizeLow property [Fax Service],IFaxAccountIncomingArchive interface, _mfax_faxaccountincomingarchive.sizelow, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizelow_cpp, fax._mfax_faxaccountincomingarchive_sizelow, faxcomex/IFaxAccountIncomingArchive::SizeLow, faxcomex/IFaxAccountIncomingArchive::get_SizeLow, get_SizeLow
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
 - IFaxAccountIncomingArchive::get_SizeLow
 - faxcomex/IFaxAccountIncomingArchive::get_SizeLow
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
 - IFaxAccountIncomingArchive.SizeLow
 - IFaxAccountIncomingArchive.get_SizeLow
 - IFaxAccountIncomingArchive.get_SizeLow
---

# IFaxAccountIncomingArchive::get_SizeLow


## -description

Specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.

This property is read-only.

## -parameters

## -remarks

Because the archive may exceed 4 GB in size, its size is described using two long values. SizeLow is the low 32-bit value of the archive size. SizeHigh is the high 32-bit value of the archive size. The size of the archive is: SizeLow + 4 GB * SizeHigh.

If both the <b>SizeLow</b> and <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-sizehigh-vb">SizeHigh</a> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive">FaxAccountIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingarchive">IFaxAccountIncomingArchive</a>