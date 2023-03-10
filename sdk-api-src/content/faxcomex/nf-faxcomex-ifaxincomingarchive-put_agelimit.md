---
UID: NF:faxcomex.IFaxIncomingArchive.put_AgeLimit
title: IFaxIncomingArchive::put_AgeLimit (faxcomex.h)
description: The AgeLimit property is a value that indicates the number of days that the fax service retains fax messages in the archive of inbound faxes. (Put)
helpviewer_keywords: ["AgeLimit property [Fax Service]","AgeLimit property [Fax Service]","IFaxIncomingArchive interface","IFaxIncomingArchive interface [Fax Service]","AgeLimit property","IFaxIncomingArchive.AgeLimit","IFaxIncomingArchive.put_AgeLimit","IFaxIncomingArchive::AgeLimit","IFaxIncomingArchive::get_AgeLimit","IFaxIncomingArchive::put_AgeLimit","_mfax_faxincomingarchive.agelimit","fax._mfax_faxincomingarchive_agelimit","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_agelimit_cpp","faxcomex/IFaxIncomingArchive::AgeLimit","faxcomex/IFaxIncomingArchive::get_AgeLimit","faxcomex/IFaxIncomingArchive::put_AgeLimit","put_AgeLimit"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_agelimit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6vjo.htm
ms.date: 12/05/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],AgeLimit property, IFaxIncomingArchive.AgeLimit, IFaxIncomingArchive.put_AgeLimit, IFaxIncomingArchive::AgeLimit, IFaxIncomingArchive::get_AgeLimit, IFaxIncomingArchive::put_AgeLimit, _mfax_faxincomingarchive.agelimit, fax._mfax_faxincomingarchive_agelimit, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_agelimit_cpp, faxcomex/IFaxIncomingArchive::AgeLimit, faxcomex/IFaxIncomingArchive::get_AgeLimit, faxcomex/IFaxIncomingArchive::put_AgeLimit, put_AgeLimit
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
 - IFaxIncomingArchive::put_AgeLimit
 - faxcomex/IFaxIncomingArchive::put_AgeLimit
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
 - IFaxIncomingArchive.AgeLimit
 - IFaxIncomingArchive.get_AgeLimit
 - IFaxIncomingArchive.put_AgeLimit
---

# IFaxIncomingArchive::put_AgeLimit


## -description

The <b>AgeLimit</b> property is a value that indicates the number of days that the fax service retains fax messages in the archive of inbound faxes. The fax service deletes messages from the inbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archiveagelimit-vb">IFaxConfiguration::put_ArchiveAgeLimit</a>   or <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archiveagelimit-vb">IFaxConfiguration::get_ArchiveAgeLimit</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>
