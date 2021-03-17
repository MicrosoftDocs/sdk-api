---
UID: NF:faxcomex.IFaxConfiguration.get_ArchiveSizeHigh
title: IFaxConfiguration::get_ArchiveSizeHigh (faxcomex.h)
description: The value that specifies the high-order 32-bit value (in bytes) for the size of the fax message archive.
helpviewer_keywords: ["ArchiveSizeHigh property [Fax Service]","ArchiveSizeHigh property [Fax Service]","IFaxConfiguration interface","IFaxConfiguration interface [Fax Service]","ArchiveSizeHigh property","IFaxConfiguration.ArchiveSizeHigh","IFaxConfiguration.get_ArchiveSizeHigh","IFaxConfiguration::ArchiveSizeHigh","IFaxConfiguration::get_ArchiveSizeHigh","fax._mfax_ifaxconfiguration_archivesizehigh","faxcomex/IFaxConfiguration::ArchiveSizeHigh","faxcomex/IFaxConfiguration::get_ArchiveSizeHigh","get_ArchiveSizeHigh"]
old-location: fax\_mfax_ifaxconfiguration_archivesizehigh.htm
tech.root: Fax
ms.assetid: 3386ec80-be4e-4105-ab57-dd634b57f67f
ms.date: 12/05/2018
ms.keywords: ArchiveSizeHigh property [Fax Service], ArchiveSizeHigh property [Fax Service],IFaxConfiguration interface, IFaxConfiguration interface [Fax Service],ArchiveSizeHigh property, IFaxConfiguration.ArchiveSizeHigh, IFaxConfiguration.get_ArchiveSizeHigh, IFaxConfiguration::ArchiveSizeHigh, IFaxConfiguration::get_ArchiveSizeHigh, fax._mfax_ifaxconfiguration_archivesizehigh, faxcomex/IFaxConfiguration::ArchiveSizeHigh, faxcomex/IFaxConfiguration::get_ArchiveSizeHigh, get_ArchiveSizeHigh
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
 - IFaxConfiguration::get_ArchiveSizeHigh
 - faxcomex/IFaxConfiguration::get_ArchiveSizeHigh
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
 - IFaxConfiguration.ArchiveSizeHigh
 - IFaxConfiguration.get_ArchiveSizeHigh
---

# IFaxConfiguration::get_ArchiveSizeHigh


## -description

The value that specifies the high-order 32-bit value (in bytes) for the size of the fax message archive.

This property is read-only.

## -parameters

## -remarks

Because the archive may exceed 4 gigabytes (GB) in size, the archive size is described using two long values. <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizelow">ArchiveSizeLow</a> is the low 32-bit value of the archive size. <b>ArchiveSizeHigh</b> is the high 32-bit value of the archive size. The size of the archive is: <b>ArchiveSizeLow</b> + 4 GB * <b>ArchiveSizeHigh</b>. 

If both the <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxconfiguration-get_archivesizelow">ArchiveSizeLow</a> and <b>ArchiveSizeHigh</b> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxconfiguration">IFaxConfiguration</a>