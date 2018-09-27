---
UID: NF:faxcomex.IFaxIncomingArchive.get_HighQuotaWaterMark
title: IFaxIncomingArchive::get_HighQuotaWaterMark
author: windows-sdk-content
description: The HighQuotaWaterMark property is a value that specifies the upper warning threshold for the size of the archive of inbound fax messages, in megabytes.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_highquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0g2z.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: HighQuotaWaterMark property [Fax Service], HighQuotaWaterMark property [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],HighQuotaWaterMark property, IFaxIncomingArchive.HighQuotaWaterMark, IFaxIncomingArchive.get_HighQuotaWaterMark, IFaxIncomingArchive.put_HighQuotaWaterMark, IFaxIncomingArchive::HighQuotaWaterMark, IFaxIncomingArchive::get_HighQuotaWaterMark, IFaxIncomingArchive::put_HighQuotaWaterMark, _mfax_faxincomingarchive.highquotawatermark, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_highquotawatermark_cpp, fax._mfax_faxincomingarchive_highquotawatermark, faxcomex/IFaxIncomingArchive::HighQuotaWaterMark, faxcomex/IFaxIncomingArchive::get_HighQuotaWaterMark, faxcomex/IFaxIncomingArchive::put_HighQuotaWaterMark, get_HighQuotaWaterMark
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
 - IFaxIncomingArchive.HighQuotaWaterMark
 - IFaxIncomingArchive.get_HighQuotaWaterMark
 - IFaxIncomingArchive.put_HighQuotaWaterMark
 - IFaxIncomingArchive.get_HighQuotaWaterMark
 - IFaxIncomingArchive.put_HighQuotaWaterMark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingArchive::get_HighQuotaWaterMark


## -description


The <b>HighQuotaWaterMark</b> property is a value that specifies the upper warning threshold for the size of the archive of inbound fax messages, in megabytes. If the size of the archive exceeds this value, and the <a href="https://msdn.microsoft.com/5b798e21-1aa8-49ee-bad3-852a5cdf659d">SizeQuotaWarning</a> property is equal to <b>TRUE</b>, the fax service issues a warning in the event log.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/2c896e7c-a110-4693-9e8d-4cbf6459c6e3">IFaxConfiguration::put_HighQuotaWaterMark</a>   or <a href="https://msdn.microsoft.com/2c896e7c-a110-4693-9e8d-4cbf6459c6e3">IFaxConfiguration::get_HighQuotaWaterMark</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/a81d6314-b26f-4946-896e-218a0095938f">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

