---
UID: NF:faxcomex.IFaxOutgoingArchive.get_SizeQuotaWarning
title: IFaxOutgoingArchive::get_SizeQuotaWarning (faxcomex.h)
description: The IFaxOutgoingArchive::get_SizeQuotaWarning property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the outbound archive exceeds the limit defined by the IFaxOutgoingArchive::get_HighQuotaWaterMark property. (Get)
helpviewer_keywords: ["IFaxOutgoingArchive interface [Fax Service]","SizeQuotaWarning property","IFaxOutgoingArchive.SizeQuotaWarning","IFaxOutgoingArchive.get_SizeQuotaWarning","IFaxOutgoingArchive.put_SizeQuotaWarning","IFaxOutgoingArchive::SizeQuotaWarning","IFaxOutgoingArchive::get_SizeQuotaWarning","IFaxOutgoingArchive::put_SizeQuotaWarning","SizeQuotaWarning property [Fax Service]","SizeQuotaWarning property [Fax Service]","IFaxOutgoingArchive interface","_mfax_faxoutgoingarchive.sizequotawarning","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizequotawarning_cpp","fax._mfax_faxoutgoingarchive_sizequotawarning","faxcomex/IFaxOutgoingArchive::SizeQuotaWarning","faxcomex/IFaxOutgoingArchive::get_SizeQuotaWarning","faxcomex/IFaxOutgoingArchive::put_SizeQuotaWarning","get_SizeQuotaWarning"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizequotawarning_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6wkn.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],SizeQuotaWarning property, IFaxOutgoingArchive.SizeQuotaWarning, IFaxOutgoingArchive.get_SizeQuotaWarning, IFaxOutgoingArchive.put_SizeQuotaWarning, IFaxOutgoingArchive::SizeQuotaWarning, IFaxOutgoingArchive::get_SizeQuotaWarning, IFaxOutgoingArchive::put_SizeQuotaWarning, SizeQuotaWarning property [Fax Service], SizeQuotaWarning property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.sizequotawarning, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizequotawarning_cpp, fax._mfax_faxoutgoingarchive_sizequotawarning, faxcomex/IFaxOutgoingArchive::SizeQuotaWarning, faxcomex/IFaxOutgoingArchive::get_SizeQuotaWarning, faxcomex/IFaxOutgoingArchive::put_SizeQuotaWarning, get_SizeQuotaWarning
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
 - IFaxOutgoingArchive::get_SizeQuotaWarning
 - faxcomex/IFaxOutgoingArchive::get_SizeQuotaWarning
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
 - IFaxOutgoingArchive.SizeQuotaWarning
 - IFaxOutgoingArchive.get_SizeQuotaWarning
 - IFaxOutgoingArchive.put_SizeQuotaWarning
 - IFaxOutgoingArchive.get_SizeQuotaWarning
 - IFaxOutgoingArchive.put_SizeQuotaWarning
---

# IFaxOutgoingArchive::get_SizeQuotaWarning


## -description

The <b>IFaxOutgoingArchive::get_SizeQuotaWarning</b> property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the outbound archive exceeds the limit defined by the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive-highquotawatermark-vb">IFaxOutgoingArchive::get_HighQuotaWaterMark</a> property.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-sizequotawarning-vb">IFaxConfiguration::put_SizeQuotaWarning</a>   or <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-sizequotawarning-vb">IFaxConfiguration::get_SizeQuotaWarning</a> method.</div>
<div> </div>
If this property is equal to <b>TRUE</b>, the fax service issues a warning when the number of fax messages in the archive exceeds the limit. If this property is equal to <b>FALSE</b>, the fax service does not issue a warning.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>
