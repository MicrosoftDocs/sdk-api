---
UID: NF:faxcomex.IFaxIncomingArchive.put_HighQuotaWaterMark
title: IFaxIncomingArchive::put_HighQuotaWaterMark (faxcomex.h)
description: The HighQuotaWaterMark property is a value that specifies the upper warning threshold for the size of the archive of inbound fax messages, in megabytes. (Put)
helpviewer_keywords: ["HighQuotaWaterMark property [Fax Service]","HighQuotaWaterMark property [Fax Service]","IFaxIncomingArchive interface","IFaxIncomingArchive interface [Fax Service]","HighQuotaWaterMark property","IFaxIncomingArchive.HighQuotaWaterMark","IFaxIncomingArchive.get_HighQuotaWaterMark","IFaxIncomingArchive.put_HighQuotaWaterMark","IFaxIncomingArchive::HighQuotaWaterMark","IFaxIncomingArchive::get_HighQuotaWaterMark","IFaxIncomingArchive::put_HighQuotaWaterMark","_mfax_faxincomingarchive.highquotawatermark","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_highquotawatermark_cpp","fax._mfax_faxincomingarchive_highquotawatermark","faxcomex/IFaxIncomingArchive::HighQuotaWaterMark","faxcomex/IFaxIncomingArchive::get_HighQuotaWaterMark","faxcomex/IFaxIncomingArchive::put_HighQuotaWaterMark","put_HighQuotaWaterMark"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_highquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0g2z.htm
ms.date: 12/05/2018
ms.keywords: HighQuotaWaterMark property [Fax Service], HighQuotaWaterMark property [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],HighQuotaWaterMark property, IFaxIncomingArchive.HighQuotaWaterMark, IFaxIncomingArchive.get_HighQuotaWaterMark, IFaxIncomingArchive.put_HighQuotaWaterMark, IFaxIncomingArchive::HighQuotaWaterMark, IFaxIncomingArchive::get_HighQuotaWaterMark, IFaxIncomingArchive::put_HighQuotaWaterMark, _mfax_faxincomingarchive.highquotawatermark, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_highquotawatermark_cpp, fax._mfax_faxincomingarchive_highquotawatermark, faxcomex/IFaxIncomingArchive::HighQuotaWaterMark, faxcomex/IFaxIncomingArchive::get_HighQuotaWaterMark, faxcomex/IFaxIncomingArchive::put_HighQuotaWaterMark, put_HighQuotaWaterMark
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
 - IFaxIncomingArchive::put_HighQuotaWaterMark
 - faxcomex/IFaxIncomingArchive::put_HighQuotaWaterMark
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
 - IFaxIncomingArchive.HighQuotaWaterMark
 - IFaxIncomingArchive.get_HighQuotaWaterMark
 - IFaxIncomingArchive.put_HighQuotaWaterMark
 - IFaxIncomingArchive.get_HighQuotaWaterMark
 - IFaxIncomingArchive.put_HighQuotaWaterMark
---

# IFaxIncomingArchive::put_HighQuotaWaterMark


## -description

The <b>HighQuotaWaterMark</b> property is a value that specifies the upper warning threshold for the size of the archive of inbound fax messages, in megabytes. If the size of the archive exceeds this value, and the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-sizequotawarning-vb">SizeQuotaWarning</a> property is equal to <b>TRUE</b>, the fax service issues a warning in the event log.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-highquotawatermark-vb">IFaxConfiguration::put_HighQuotaWaterMark</a>   or <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-highquotawatermark-vb">IFaxConfiguration::get_HighQuotaWaterMark</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>
