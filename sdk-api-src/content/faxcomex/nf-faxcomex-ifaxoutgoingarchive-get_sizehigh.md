---
UID: NF:faxcomex.IFaxOutgoingArchive.get_SizeHigh
title: IFaxOutgoingArchive::get_SizeHigh (faxcomex.h)
description: The IFaxOutgoingArchive::get_SizeHigh property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of outgoing fax messages.
helpviewer_keywords: ["IFaxOutgoingArchive interface [Fax Service]","SizeHigh property","IFaxOutgoingArchive.SizeHigh","IFaxOutgoingArchive.get_SizeHigh","IFaxOutgoingArchive::SizeHigh","IFaxOutgoingArchive::get_SizeHigh","SizeHigh property [Fax Service]","SizeHigh property [Fax Service]","IFaxOutgoingArchive interface","_mfax_faxoutgoingarchive.sizehigh","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizehigh_cpp","fax._mfax_faxoutgoingarchive_sizehigh","faxcomex/IFaxOutgoingArchive::SizeHigh","faxcomex/IFaxOutgoingArchive::get_SizeHigh","get_SizeHigh"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizehigh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4je0.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],SizeHigh property, IFaxOutgoingArchive.SizeHigh, IFaxOutgoingArchive.get_SizeHigh, IFaxOutgoingArchive::SizeHigh, IFaxOutgoingArchive::get_SizeHigh, SizeHigh property [Fax Service], SizeHigh property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.sizehigh, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizehigh_cpp, fax._mfax_faxoutgoingarchive_sizehigh, faxcomex/IFaxOutgoingArchive::SizeHigh, faxcomex/IFaxOutgoingArchive::get_SizeHigh, get_SizeHigh
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
 - IFaxOutgoingArchive::get_SizeHigh
 - faxcomex/IFaxOutgoingArchive::get_SizeHigh
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
 - IFaxOutgoingArchive.SizeHigh
 - IFaxOutgoingArchive.get_SizeHigh
 - IFaxOutgoingArchive.get_SizeHigh
---

# IFaxOutgoingArchive::get_SizeHigh


## -description

The <b>IFaxOutgoingArchive::get_SizeHigh</b> property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of outgoing fax messages.

This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizehigh">IFaxConfiguration::get_ArchiveSizeHigh</a> method.</div>
<div> </div>
Because the archive may exceed 4 gigabytes (GB) in size, the archive size is described using two long values. <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive-sizelow-vb">SizeLow</a> is the low 32-bit value of the archive size. <b>SizeHigh</b> is the high 32-bit value of the archive size. The size of the archive is: <b>SizeLow</b> + 4 GB * <b>SizeHigh</b>. If both the <b>SizeLow</b> and <b>SizeHigh</b> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>