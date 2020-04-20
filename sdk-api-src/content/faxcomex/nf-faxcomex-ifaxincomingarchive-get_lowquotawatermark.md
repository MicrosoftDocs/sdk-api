---
UID: NF:faxcomex.IFaxIncomingArchive.get_LowQuotaWaterMark
title: IFaxIncomingArchive::get_LowQuotaWaterMark (faxcomex.h)
description: The LowQuotaWaterMark property is a value that specifies the lower warning threshold for the archive of inbound fax messages, in megabytes.helpviewer_keywords: ["IFaxIncomingArchive interface [Fax Service]","LowQuotaWaterMark property","IFaxIncomingArchive.LowQuotaWaterMark","IFaxIncomingArchive.get_LowQuotaWaterMark","IFaxIncomingArchive.put_LowQuotaWaterMark","IFaxIncomingArchive::LowQuotaWaterMark","IFaxIncomingArchive::get_LowQuotaWaterMark","IFaxIncomingArchive::put_LowQuotaWaterMark","LowQuotaWaterMark property [Fax Service]","LowQuotaWaterMark property [Fax Service]","IFaxIncomingArchive interface","_mfax_faxincomingarchive.lowquotawatermark","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_lowquotawatermark_cpp","fax._mfax_faxincomingarchive_lowquotawatermark","faxcomex/IFaxIncomingArchive::LowQuotaWaterMark","faxcomex/IFaxIncomingArchive::get_LowQuotaWaterMark","faxcomex/IFaxIncomingArchive::put_LowQuotaWaterMark","get_LowQuotaWaterMark"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_lowquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1lkb.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],LowQuotaWaterMark property, IFaxIncomingArchive.LowQuotaWaterMark, IFaxIncomingArchive.get_LowQuotaWaterMark, IFaxIncomingArchive.put_LowQuotaWaterMark, IFaxIncomingArchive::LowQuotaWaterMark, IFaxIncomingArchive::get_LowQuotaWaterMark, IFaxIncomingArchive::put_LowQuotaWaterMark, LowQuotaWaterMark property [Fax Service], LowQuotaWaterMark property [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.lowquotawatermark, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_lowquotawatermark_cpp, fax._mfax_faxincomingarchive_lowquotawatermark, faxcomex/IFaxIncomingArchive::LowQuotaWaterMark, faxcomex/IFaxIncomingArchive::get_LowQuotaWaterMark, faxcomex/IFaxIncomingArchive::put_LowQuotaWaterMark, get_LowQuotaWaterMark
f1_keywords:
- faxcomex/IFaxIncomingArchive.LowQuotaWaterMark
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
- IFaxIncomingArchive.LowQuotaWaterMark
- IFaxIncomingArchive.get_LowQuotaWaterMark
- IFaxIncomingArchive.put_LowQuotaWaterMark
- IFaxIncomingArchive.get_LowQuotaWaterMark
- IFaxIncomingArchive.put_LowQuotaWaterMark
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingArchive::get_LowQuotaWaterMark


## -description


The <b>LowQuotaWaterMark</b> property is a value that specifies the lower warning threshold for the archive of inbound fax messages, in megabytes. If the fax service has issued a warning in the event log, the service does not issue additional warnings until the size of the inbound archive drops below this value.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-lowquotawatermark-vb">IFaxConfiguration::put_LowQuotaWaterMark</a>   or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-lowquotawatermark-vb">IFaxConfiguration::get_LowQuotaWaterMark</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>
 

 

