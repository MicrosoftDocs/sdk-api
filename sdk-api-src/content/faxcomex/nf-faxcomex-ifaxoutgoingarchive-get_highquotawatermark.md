---
UID: NF:faxcomex.IFaxOutgoingArchive.get_HighQuotaWaterMark
title: IFaxOutgoingArchive::get_HighQuotaWaterMark
author: windows-sdk-content
description: The IFaxOutgoingArchive::get_HighQuotaWaterMark property is a value that specifies the upper threshold for the size of the archive of inbound fax messages, in megabytes.
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_highquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_64tn.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: HighQuotaWaterMark property [Fax Service], HighQuotaWaterMark property [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],HighQuotaWaterMark property, IFaxOutgoingArchive.HighQuotaWaterMark, IFaxOutgoingArchive.get_HighQuotaWaterMark, IFaxOutgoingArchive.put_HighQuotaWaterMark, IFaxOutgoingArchive::HighQuotaWaterMark, IFaxOutgoingArchive::get_HighQuotaWaterMark, IFaxOutgoingArchive::put_HighQuotaWaterMark, _mfax_faxoutgoingarchive.highquotawatermark, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_highquotawatermark_cpp, fax._mfax_faxoutgoingarchive_highquotawatermark, faxcomex/IFaxOutgoingArchive::HighQuotaWaterMark, faxcomex/IFaxOutgoingArchive::get_HighQuotaWaterMark, faxcomex/IFaxOutgoingArchive::put_HighQuotaWaterMark, get_HighQuotaWaterMark
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingArchive::get_HighQuotaWaterMark


## -description


The <b>IFaxOutgoingArchive::get_HighQuotaWaterMark</b> property is a value that specifies the upper threshold for the size of the archive of inbound fax messages, in megabytes. If the archived fax messages in the archive exceed this value, and the <a href="https://msdn.microsoft.com/28c5eb64-7382-4968-82e7-fd2f79798e41">IFaxOutgoingArchive::get_SizeQuotaWarning</a> property is equal to <b>TRUE</b>, the fax service issues a warning in the event log.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/2c896e7c-a110-4693-9e8d-4cbf6459c6e3">IFaxConfiguration::put_HighQuotaWaterMark</a>   or <a href="https://msdn.microsoft.com/2c896e7c-a110-4693-9e8d-4cbf6459c6e3">IFaxConfiguration::get_HighQuotaWaterMark</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/68f6c0f2-ea06-401c-9021-c50940f8cd7a">Visual Basic Example</a>
 

 

