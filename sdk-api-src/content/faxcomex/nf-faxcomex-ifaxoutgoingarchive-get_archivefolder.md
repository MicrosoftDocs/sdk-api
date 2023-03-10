---
UID: NF:faxcomex.IFaxOutgoingArchive.get_ArchiveFolder
title: IFaxOutgoingArchive::get_ArchiveFolder (faxcomex.h)
description: The IFaxOutgoingArchive::get_ArchiveFolder property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes. (Get)
helpviewer_keywords: ["ArchiveFolder property [Fax Service]","ArchiveFolder property [Fax Service]","IFaxOutgoingArchive interface","IFaxOutgoingArchive interface [Fax Service]","ArchiveFolder property","IFaxOutgoingArchive.ArchiveFolder","IFaxOutgoingArchive.get_ArchiveFolder","IFaxOutgoingArchive::ArchiveFolder","IFaxOutgoingArchive::get_ArchiveFolder","IFaxOutgoingArchive::put_ArchiveFolder","_mfax_faxoutgoingarchive.archivefolder","fax._mfax_faxoutgoingarchive_archivefolder","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_archivefolder_cpp","faxcomex/IFaxOutgoingArchive::ArchiveFolder","faxcomex/IFaxOutgoingArchive::get_ArchiveFolder","faxcomex/IFaxOutgoingArchive::put_ArchiveFolder","get_ArchiveFolder"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_archivefolder_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4302.htm
ms.date: 12/05/2018
ms.keywords: ArchiveFolder property [Fax Service], ArchiveFolder property [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],ArchiveFolder property, IFaxOutgoingArchive.ArchiveFolder, IFaxOutgoingArchive.get_ArchiveFolder, IFaxOutgoingArchive::ArchiveFolder, IFaxOutgoingArchive::get_ArchiveFolder, IFaxOutgoingArchive::put_ArchiveFolder, _mfax_faxoutgoingarchive.archivefolder, fax._mfax_faxoutgoingarchive_archivefolder, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_archivefolder_cpp, faxcomex/IFaxOutgoingArchive::ArchiveFolder, faxcomex/IFaxOutgoingArchive::get_ArchiveFolder, faxcomex/IFaxOutgoingArchive::put_ArchiveFolder, get_ArchiveFolder
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
 - IFaxOutgoingArchive::get_ArchiveFolder
 - faxcomex/IFaxOutgoingArchive::get_ArchiveFolder
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
 - IFaxOutgoingArchive.ArchiveFolder
 - IFaxOutgoingArchive.get_ArchiveFolder
 - IFaxOutgoingArchive.put_ArchiveFolder
---

# IFaxOutgoingArchive::get_ArchiveFolder


## -description

The <b>IFaxOutgoingArchive::get_ArchiveFolder</b> property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> interface, and then call the  <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archivelocation-vb">IFaxConfiguration::put_ArchiveLocation</a>   or <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-archivelocation-vb">IFaxConfiguration::get_ArchiveLocation</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>
