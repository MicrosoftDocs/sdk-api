---
UID: NF:faxcomex.IFaxOutgoingArchive.get_AgeLimit
title: IFaxOutgoingArchive::get_AgeLimit (faxcomex.h)
description: The IFaxOutgoingArchive::get_AgeLimit property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes. (Get)
helpviewer_keywords: ["AgeLimit property [Fax Service]","AgeLimit property [Fax Service]","IFaxOutgoingArchive interface","IFaxOutgoingArchive interface [Fax Service]","AgeLimit property","IFaxOutgoingArchive.AgeLimit","IFaxOutgoingArchive.get_AgeLimit","IFaxOutgoingArchive::AgeLimit","IFaxOutgoingArchive::get_AgeLimit","IFaxOutgoingArchive::put_AgeLimit","_mfax_faxoutgoingarchive.agelimit","fax._mfax_faxoutgoingarchive_agelimit","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_agelimit_cpp","faxcomex/IFaxOutgoingArchive::AgeLimit","faxcomex/IFaxOutgoingArchive::get_AgeLimit","faxcomex/IFaxOutgoingArchive::put_AgeLimit","get_AgeLimit"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_agelimit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_69mc.htm
ms.date: 12/05/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],AgeLimit property, IFaxOutgoingArchive.AgeLimit, IFaxOutgoingArchive.get_AgeLimit, IFaxOutgoingArchive::AgeLimit, IFaxOutgoingArchive::get_AgeLimit, IFaxOutgoingArchive::put_AgeLimit, _mfax_faxoutgoingarchive.agelimit, fax._mfax_faxoutgoingarchive_agelimit, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_agelimit_cpp, faxcomex/IFaxOutgoingArchive::AgeLimit, faxcomex/IFaxOutgoingArchive::get_AgeLimit, faxcomex/IFaxOutgoingArchive::put_AgeLimit, get_AgeLimit
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
 - IFaxOutgoingArchive::get_AgeLimit
 - faxcomex/IFaxOutgoingArchive::get_AgeLimit
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
 - IFaxOutgoingArchive.AgeLimit
 - IFaxOutgoingArchive.get_AgeLimit
 - IFaxOutgoingArchive.put_AgeLimit
---

# IFaxOutgoingArchive::get_AgeLimit


## -description

The <b>IFaxOutgoingArchive::get_AgeLimit</b> property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes. The fax service deletes messages from the outbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archiveagelimit-vb">IFaxConfiguration::put_ArchiveAgeLimit</a>   or <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archiveagelimit-vb">IFaxConfiguration::get_ArchiveAgeLimit</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>
