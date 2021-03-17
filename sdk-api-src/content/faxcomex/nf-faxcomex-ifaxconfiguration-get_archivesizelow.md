---
UID: NF:faxcomex.IFaxConfiguration.get_ArchiveSizeLow
title: IFaxConfiguration::get_ArchiveSizeLow (faxcomex.h)
description: The value that specifies the low-order 32-bit value (in bytes) for the size of the fax message archive.
helpviewer_keywords: ["ArchiveSizeLow property [Fax Service]","ArchiveSizeLow property [Fax Service]","IFaxConfiguration interface","IFaxConfiguration interface [Fax Service]","ArchiveSizeLow property","IFaxConfiguration.ArchiveSizeLow","IFaxConfiguration.get_ArchiveSizeLow","IFaxConfiguration::ArchiveSizeLow","IFaxConfiguration::get_ArchiveSizeLow","fax._mfax_ifaxconfiguration_archivesizelow","faxcomex/IFaxConfiguration::ArchiveSizeLow","faxcomex/IFaxConfiguration::get_ArchiveSizeLow","get_ArchiveSizeLow"]
old-location: fax\_mfax_ifaxconfiguration_archivesizelow.htm
tech.root: Fax
ms.assetid: e10cde26-deec-47b8-bc69-0b785087ab74
ms.date: 12/05/2018
ms.keywords: ArchiveSizeLow property [Fax Service], ArchiveSizeLow property [Fax Service],IFaxConfiguration interface, IFaxConfiguration interface [Fax Service],ArchiveSizeLow property, IFaxConfiguration.ArchiveSizeLow, IFaxConfiguration.get_ArchiveSizeLow, IFaxConfiguration::ArchiveSizeLow, IFaxConfiguration::get_ArchiveSizeLow, fax._mfax_ifaxconfiguration_archivesizelow, faxcomex/IFaxConfiguration::ArchiveSizeLow, faxcomex/IFaxConfiguration::get_ArchiveSizeLow, get_ArchiveSizeLow
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Faxcomex.idl
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
 - IFaxConfiguration::get_ArchiveSizeLow
 - faxcomex/IFaxConfiguration::get_ArchiveSizeLow
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
 - IFaxConfiguration.ArchiveSizeLow
 - IFaxConfiguration.get_ArchiveSizeLow
---

# IFaxConfiguration::get_ArchiveSizeLow


## -description

The value that specifies the low-order 32-bit value (in bytes) for the size of the fax message archive.

This property is read-only.

## -parameters

## -remarks

Because the archive may exceed 4 gigabytes (GB) in size, the archive size is described using two long values. <b>ArchiveSizeLow</b> is the low 32-bit value of the archive size. <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizehigh">ArchiveSizeHigh</a> is the high 32-bit value of the archive size. The size of the archive is: <b>ArchiveSizeLow</b> + 4 GB * <b>ArchiveSizeHigh</b>. 

If both the <b>ArchiveSizeLow</b> and <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizehigh">ArchiveSizeHigh</a> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a>