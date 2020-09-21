---
UID: NF:faxcomex.IFaxIncomingArchive.get_SizeHigh
title: IFaxIncomingArchive::get_SizeHigh (faxcomex.h)
description: The SizeHigh property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of inbound fax messages.
helpviewer_keywords: ["IFaxIncomingArchive interface [Fax Service]","SizeHigh property","IFaxIncomingArchive.SizeHigh","IFaxIncomingArchive.get_SizeHigh","IFaxIncomingArchive::SizeHigh","IFaxIncomingArchive::get_SizeHigh","SizeHigh property [Fax Service]","SizeHigh property [Fax Service]","IFaxIncomingArchive interface","_mfax_faxincomingarchive.sizehigh","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizehigh_cpp","fax._mfax_faxincomingarchive_sizehigh","faxcomex/IFaxIncomingArchive::SizeHigh","faxcomex/IFaxIncomingArchive::get_SizeHigh","get_SizeHigh"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizehigh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_55bc.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],SizeHigh property, IFaxIncomingArchive.SizeHigh, IFaxIncomingArchive.get_SizeHigh, IFaxIncomingArchive::SizeHigh, IFaxIncomingArchive::get_SizeHigh, SizeHigh property [Fax Service], SizeHigh property [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.sizehigh, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizehigh_cpp, fax._mfax_faxincomingarchive_sizehigh, faxcomex/IFaxIncomingArchive::SizeHigh, faxcomex/IFaxIncomingArchive::get_SizeHigh, get_SizeHigh
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
 - IFaxIncomingArchive::get_SizeHigh
 - faxcomex/IFaxIncomingArchive::get_SizeHigh
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
 - IFaxIncomingArchive.SizeHigh
 - IFaxIncomingArchive.get_SizeHigh
 - IFaxIncomingArchive.get_SizeHigh
---

# IFaxIncomingArchive::get_SizeHigh


## -description

The <b>SizeHigh</b> property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of inbound fax messages.

This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows.</div>
<div> </div>
Because the archive may exceed 4 GB in size, the archive's size is described using two long values. SizeLow is the low 32-bit value of the archive size. SizeHigh is the high 32-bit value of the archive size. The size of the archive is: SizeLow + 4 GB * SizeHigh.

If both the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizelow-vb">SizeLow</a> and <b>SizeHigh</b> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>