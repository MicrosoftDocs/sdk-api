---
UID: NF:faxcomex.IFaxOutgoingArchive.get_SizeLow
title: IFaxOutgoingArchive::get_SizeLow (faxcomex.h)
description: The IFaxOutgoingArchive::get_SizeLow property is a value that specifies the low 32-bit value (in bytes) for the size of the archive of outgoing fax messages.
helpviewer_keywords: ["IFaxOutgoingArchive interface [Fax Service]","SizeLow property","IFaxOutgoingArchive.SizeLow","IFaxOutgoingArchive.get_SizeLow","IFaxOutgoingArchive::SizeLow","IFaxOutgoingArchive::get_SizeLow","SizeLow property [Fax Service]","SizeLow property [Fax Service]","IFaxOutgoingArchive interface","_mfax_faxoutgoingarchive.sizelow","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizelow_cpp","fax._mfax_faxoutgoingarchive_sizelow","faxcomex/IFaxOutgoingArchive::SizeLow","faxcomex/IFaxOutgoingArchive::get_SizeLow","get_SizeLow"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizelow_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8v93.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],SizeLow property, IFaxOutgoingArchive.SizeLow, IFaxOutgoingArchive.get_SizeLow, IFaxOutgoingArchive::SizeLow, IFaxOutgoingArchive::get_SizeLow, SizeLow property [Fax Service], SizeLow property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.sizelow, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizelow_cpp, fax._mfax_faxoutgoingarchive_sizelow, faxcomex/IFaxOutgoingArchive::SizeLow, faxcomex/IFaxOutgoingArchive::get_SizeLow, get_SizeLow
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
 - IFaxOutgoingArchive::get_SizeLow
 - faxcomex/IFaxOutgoingArchive::get_SizeLow
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
 - IFaxOutgoingArchive.SizeLow
 - IFaxOutgoingArchive.get_SizeLow
 - IFaxOutgoingArchive.get_SizeLow
---

# IFaxOutgoingArchive::get_SizeLow


## -description

The <b>IFaxOutgoingArchive::get_SizeLow</b> property is a value that specifies the low 32-bit value (in bytes) for the size of the archive of outgoing fax messages.

This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizelow">IFaxConfiguration::get_ArchiveSizeLow</a> method.</div>
<div> </div>
Because the archive may exceed 4 gigabytes (GB) in size, the archive size is described using two long values. <b>SizeLow</b> is the low 32-bit value of the archive size. <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive-sizehigh-vb">SizeHigh</a> is the high 32-bit value of the archive size. The size of the archive is: <b>SizeLow</b> + 4 GB * <b>SizeHigh</b>. If both the <b>SizeLow</b> and <b>SizeHigh</b> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>