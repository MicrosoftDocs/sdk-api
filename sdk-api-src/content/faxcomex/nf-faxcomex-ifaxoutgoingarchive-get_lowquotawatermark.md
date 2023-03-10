---
UID: NF:faxcomex.IFaxOutgoingArchive.get_LowQuotaWaterMark
title: IFaxOutgoingArchive::get_LowQuotaWaterMark (faxcomex.h)
description: The IFaxOutgoingArchive::get_LowQuotaWaterMark property is a value that specifies the lower threshold for the archive of outbound fax messages, in megabytes. (Get)
helpviewer_keywords: ["IFaxOutgoingArchive interface [Fax Service]","LowQuotaWaterMark property","IFaxOutgoingArchive.LowQuotaWaterMark","IFaxOutgoingArchive.get_LowQuotaWaterMark","IFaxOutgoingArchive.put_LowQuotaWaterMark","IFaxOutgoingArchive::LowQuotaWaterMark","IFaxOutgoingArchive::get_LowQuotaWaterMark","IFaxOutgoingArchive::put_LowQuotaWaterMark","LowQuotaWaterMark property [Fax Service]","LowQuotaWaterMark property [Fax Service]","IFaxOutgoingArchive interface","_mfax_faxoutgoingarchive.lowquotawatermark","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_lowquotawatermark_cpp","fax._mfax_faxoutgoingarchive_lowquotawatermark","faxcomex/IFaxOutgoingArchive::LowQuotaWaterMark","faxcomex/IFaxOutgoingArchive::get_LowQuotaWaterMark","faxcomex/IFaxOutgoingArchive::put_LowQuotaWaterMark","get_LowQuotaWaterMark"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_lowquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9nmz.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],LowQuotaWaterMark property, IFaxOutgoingArchive.LowQuotaWaterMark, IFaxOutgoingArchive.get_LowQuotaWaterMark, IFaxOutgoingArchive.put_LowQuotaWaterMark, IFaxOutgoingArchive::LowQuotaWaterMark, IFaxOutgoingArchive::get_LowQuotaWaterMark, IFaxOutgoingArchive::put_LowQuotaWaterMark, LowQuotaWaterMark property [Fax Service], LowQuotaWaterMark property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.lowquotawatermark, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_lowquotawatermark_cpp, fax._mfax_faxoutgoingarchive_lowquotawatermark, faxcomex/IFaxOutgoingArchive::LowQuotaWaterMark, faxcomex/IFaxOutgoingArchive::get_LowQuotaWaterMark, faxcomex/IFaxOutgoingArchive::put_LowQuotaWaterMark, get_LowQuotaWaterMark
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
 - IFaxOutgoingArchive::get_LowQuotaWaterMark
 - faxcomex/IFaxOutgoingArchive::get_LowQuotaWaterMark
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
 - IFaxOutgoingArchive.LowQuotaWaterMark
 - IFaxOutgoingArchive.get_LowQuotaWaterMark
 - IFaxOutgoingArchive.put_LowQuotaWaterMark
 - IFaxOutgoingArchive.get_LowQuotaWaterMark
 - IFaxOutgoingArchive.put_LowQuotaWaterMark
---

# IFaxOutgoingArchive::get_LowQuotaWaterMark


## -description

The <b>IFaxOutgoingArchive::get_LowQuotaWaterMark</b> property is a value that specifies the lower threshold for the archive of outbound fax messages, in megabytes. If the fax service has issued a warning in the event log, the service does not issue additional warnings until the size of the outbound archive drops below this value. 

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-lowquotawatermark-vb">IFaxConfiguration::put_LowQuotaWaterMark</a>   or <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-lowquotawatermark-vb">IFaxConfiguration::get_LowQuotaWaterMark</a> method.</div>
<div> </div>
To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>
