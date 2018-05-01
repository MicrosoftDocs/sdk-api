---
UID: NF:faxcomex.IFaxConfiguration.get_ArchiveSizeHigh
title: IFaxConfiguration::get_ArchiveSizeHigh method
author: windows-driver-content
description: The value that specifies the high-order 32-bit value (in bytes) for the size of the fax message archive.
old-location: fax\_mfax_ifaxconfiguration_archivesizehigh.htm
old-project: Fax
ms.assetid: 3386ec80-be4e-4105-ab57-dd634b57f67f
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: ArchiveSizeHigh property [Fax Service], ArchiveSizeHigh property [Fax Service], IFaxConfiguration interface, IFaxConfiguration, IFaxConfiguration interface [Fax Service], ArchiveSizeHigh property, IFaxConfiguration.ArchiveSizeHigh, IFaxConfiguration::get_ArchiveSizeHigh, fax._mfax_ifaxconfiguration_archivesizehigh, faxcomex/IFaxConfiguration::ArchiveSizeHigh, faxcomex/IFaxConfiguration::get_ArchiveSizeHigh, get_ArchiveSizeHigh,IFaxConfiguration.get_ArchiveSizeHigh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxConfiguration.ArchiveSizeHigh
-	IFaxConfiguration.get_ArchiveSizeHigh
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxConfiguration::get_ArchiveSizeHigh method


## -description


The value that specifies the high-order 32-bit value (in bytes) for the size of the fax message archive.

This property is read-only.


## -parameters


## -remarks



Because the archive may exceed 4 gigabytes (GB) in size, the archive size is described using two long values. <a href="https://msdn.microsoft.com/e10cde26-deec-47b8-bc69-0b785087ab74">ArchiveSizeLow</a> is the low 32-bit value of the archive size. <b>ArchiveSizeHigh</b> is the high 32-bit value of the archive size. The size of the archive is: <b>ArchiveSizeLow</b> + 4 GB * <b>ArchiveSizeHigh</b>. 

If both the <a href="https://msdn.microsoft.com/e10cde26-deec-47b8-bc69-0b785087ab74">ArchiveSizeLow</a> and <b>ArchiveSizeHigh</b> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a>
 

 

