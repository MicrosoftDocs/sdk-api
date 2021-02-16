---
UID: NF:faxcomex.IFaxIncomingArchive.get_SizeLow
title: IFaxIncomingArchive::get_SizeLow (faxcomex.h)
description: The SizeLow property is a value that specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages.
helpviewer_keywords: ["IFaxIncomingArchive interface [Fax Service]","SizeLow property","IFaxIncomingArchive.SizeLow","IFaxIncomingArchive.get_SizeLow","IFaxIncomingArchive::SizeLow","IFaxIncomingArchive::get_SizeLow","SizeLow property [Fax Service]","SizeLow property [Fax Service]","IFaxIncomingArchive interface","_mfax_faxincomingarchive.sizelow","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizelow_cpp","fax._mfax_faxincomingarchive_sizelow","faxcomex/IFaxIncomingArchive::SizeLow","faxcomex/IFaxIncomingArchive::get_SizeLow","get_SizeLow"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizelow_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0fuf.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],SizeLow property, IFaxIncomingArchive.SizeLow, IFaxIncomingArchive.get_SizeLow, IFaxIncomingArchive::SizeLow, IFaxIncomingArchive::get_SizeLow, SizeLow property [Fax Service], SizeLow property [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.sizelow, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizelow_cpp, fax._mfax_faxincomingarchive_sizelow, faxcomex/IFaxIncomingArchive::SizeLow, faxcomex/IFaxIncomingArchive::get_SizeLow, get_SizeLow
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
 - IFaxIncomingArchive::get_SizeLow
 - faxcomex/IFaxIncomingArchive::get_SizeLow
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
 - IFaxIncomingArchive.SizeLow
 - IFaxIncomingArchive.get_SizeLow
 - IFaxIncomingArchive.get_SizeLow
---

# IFaxIncomingArchive::get_SizeLow


## -description

The <b>SizeLow</b> property is a value that specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages.

This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows.</div>
<div> </div>
Because the archive may exceed 4 GB in size, the archive's size is described using two long values. SizeLow is the low 32-bit value of the archive size. SizeHigh is the high 32-bit value of the archive size. The size of the archive is: SizeLow + 4 GB * SizeHigh.

If both the <b>SizeLow</b> and <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizehigh-vb">SizeHigh</a> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>