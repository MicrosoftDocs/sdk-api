---
UID: NF:faxcomex.IFaxOutgoingArchive.put_HighQuotaWaterMark
title: IFaxOutgoingArchive::put_HighQuotaWaterMark (faxcomex.h)
description: The IFaxOutgoingArchive::get_HighQuotaWaterMark property is a value that specifies the upper threshold for the size of the archive of inbound fax messages, in megabytes.helpviewer_keywords: ["HighQuotaWaterMark property [Fax Service]","HighQuotaWaterMark property [Fax Service]","IFaxOutgoingArchive interface","IFaxOutgoingArchive interface [Fax Service]","HighQuotaWaterMark property","IFaxOutgoingArchive.HighQuotaWaterMark","IFaxOutgoingArchive.get_HighQuotaWaterMark","IFaxOutgoingArchive.put_HighQuotaWaterMark","IFaxOutgoingArchive::HighQuotaWaterMark","IFaxOutgoingArchive::get_HighQuotaWaterMark","IFaxOutgoingArchive::put_HighQuotaWaterMark","_mfax_faxoutgoingarchive.highquotawatermark","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_highquotawatermark_cpp","fax._mfax_faxoutgoingarchive_highquotawatermark","faxcomex/IFaxOutgoingArchive::HighQuotaWaterMark","faxcomex/IFaxOutgoingArchive::get_HighQuotaWaterMark","faxcomex/IFaxOutgoingArchive::put_HighQuotaWaterMark","put_HighQuotaWaterMark"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_highquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_64tn.htm
ms.date: 12/05/2018
ms.keywords: HighQuotaWaterMark property [Fax Service], HighQuotaWaterMark property [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],HighQuotaWaterMark property, IFaxOutgoingArchive.HighQuotaWaterMark, IFaxOutgoingArchive.get_HighQuotaWaterMark, IFaxOutgoingArchive.put_HighQuotaWaterMark, IFaxOutgoingArchive::HighQuotaWaterMark, IFaxOutgoingArchive::get_HighQuotaWaterMark, IFaxOutgoingArchive::put_HighQuotaWaterMark, _mfax_faxoutgoingarchive.highquotawatermark, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_highquotawatermark_cpp, fax._mfax_faxoutgoingarchive_highquotawatermark, faxcomex/IFaxOutgoingArchive::HighQuotaWaterMark, faxcomex/IFaxOutgoingArchive::get_HighQuotaWaterMark, faxcomex/IFaxOutgoingArchive::put_HighQuotaWaterMark, put_HighQuotaWaterMark
f1_keywords:
- faxcomex/IFaxOutgoingArchive.HighQuotaWaterMark
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Fxscomex.dll
api_name:
- IFaxOutgoingArchive.HighQuotaWaterMark
- IFaxOutgoingArchive.get_HighQuotaWaterMark
- IFaxOutgoingArchive.put_HighQuotaWaterMark
- IFaxOutgoingArchive.get_HighQuotaWaterMark
- IFaxOutgoingArchive.put_HighQuotaWaterMark
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutgoingArchive::put_HighQuotaWaterMark


## -description


The <b>IFaxOutgoingArchive::get_HighQuotaWaterMark</b> property is a value that specifies the upper threshold for the size of the archive of inbound fax messages, in megabytes. If the archived fax messages in the archive exceed this value, and the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive-sizequotawarning-vb">IFaxOutgoingArchive::get_SizeQuotaWarning</a> property is equal to <b>TRUE</b>, the fax service issues a warning in the event log.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-highquotawatermark-vb">IFaxConfiguration::put_HighQuotaWaterMark</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-highquotawatermark-vb">IFaxConfiguration::get_HighQuotaWaterMark</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>
 

 

