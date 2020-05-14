---
UID: NF:faxcomex.IFaxAccountIncomingArchive.get_SizeHigh
title: IFaxAccountIncomingArchive::get_SizeHigh (faxcomex.h)
description: Specifies the high 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.helpviewer_keywords: ["IFaxAccountIncomingArchive interface [Fax Service]","SizeHigh property","IFaxAccountIncomingArchive.SizeHigh","IFaxAccountIncomingArchive.get_SizeHigh","IFaxAccountIncomingArchive::SizeHigh","IFaxAccountIncomingArchive::get_SizeHigh","SizeHigh property [Fax Service]","SizeHigh property [Fax Service]","IFaxAccountIncomingArchive interface","_mfax_faxaccountincomingarchive.sizehigh","fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizehigh_cpp","fax._mfax_faxaccountincomingarchive_sizehigh","faxcomex/IFaxAccountIncomingArchive::SizeHigh","faxcomex/IFaxAccountIncomingArchive::get_SizeHigh","get_SizeHigh"]
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizehigh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\sizehigh.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountIncomingArchive interface [Fax Service],SizeHigh property, IFaxAccountIncomingArchive.SizeHigh, IFaxAccountIncomingArchive.get_SizeHigh, IFaxAccountIncomingArchive::SizeHigh, IFaxAccountIncomingArchive::get_SizeHigh, SizeHigh property [Fax Service], SizeHigh property [Fax Service],IFaxAccountIncomingArchive interface, _mfax_faxaccountincomingarchive.sizehigh, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizehigh_cpp, fax._mfax_faxaccountincomingarchive_sizehigh, faxcomex/IFaxAccountIncomingArchive::SizeHigh, faxcomex/IFaxAccountIncomingArchive::get_SizeHigh, get_SizeHigh
f1_keywords:
- faxcomex/IFaxAccountIncomingArchive.SizeHigh
dev_langs:
- c++
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
- IFaxAccountIncomingArchive.SizeHigh
- IFaxAccountIncomingArchive.get_SizeHigh
- IFaxAccountIncomingArchive.get_SizeHigh
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxAccountIncomingArchive::get_SizeHigh


## -description


Specifies the high 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.

This property is read-only.


## -parameters


## -remarks



Because the archive may exceed 4 GB in size, its size is described using two long values. SizeLow is the low 32-bit value of the archive size. SizeHigh is the high 32-bit value of the archive size. The size of the archive is: SizeLow + 4 GB * SizeHigh.

If both the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-sizelow-vb">SizeLow</a> and <b>SizeHigh</b> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

The property is read-only.

To read this property, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive">FaxAccountIncomingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingarchive">IFaxAccountIncomingArchive</a>
 

 

