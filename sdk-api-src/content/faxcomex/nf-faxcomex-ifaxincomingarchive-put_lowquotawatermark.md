---
UID: NF:faxcomex.IFaxIncomingArchive.put_LowQuotaWaterMark
title: IFaxIncomingArchive::put_LowQuotaWaterMark
author: windows-sdk-content
description: The LowQuotaWaterMark property is a value that specifies the lower warning threshold for the archive of inbound fax messages, in megabytes.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_lowquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1lkb.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],LowQuotaWaterMark property, IFaxIncomingArchive.LowQuotaWaterMark, IFaxIncomingArchive.get_LowQuotaWaterMark, IFaxIncomingArchive.put_LowQuotaWaterMark, IFaxIncomingArchive::LowQuotaWaterMark, IFaxIncomingArchive::get_LowQuotaWaterMark, IFaxIncomingArchive::put_LowQuotaWaterMark, LowQuotaWaterMark property [Fax Service], LowQuotaWaterMark property [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.lowquotawatermark, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_lowquotawatermark_cpp, fax._mfax_faxincomingarchive_lowquotawatermark, faxcomex/IFaxIncomingArchive::LowQuotaWaterMark, faxcomex/IFaxIncomingArchive::get_LowQuotaWaterMark, faxcomex/IFaxIncomingArchive::put_LowQuotaWaterMark, put_LowQuotaWaterMark
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
 - IFaxIncomingArchive.LowQuotaWaterMark
 - IFaxIncomingArchive.get_LowQuotaWaterMark
 - IFaxIncomingArchive.put_LowQuotaWaterMark
 - IFaxIncomingArchive.get_LowQuotaWaterMark
 - IFaxIncomingArchive.put_LowQuotaWaterMark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingArchive::put_LowQuotaWaterMark


## -description


The <b>LowQuotaWaterMark</b> property is a value that specifies the lower warning threshold for the archive of inbound fax messages, in megabytes. If the fax service has issued a warning in the event log, the service does not issue additional warnings until the size of the inbound archive drops below this value.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/939cf7c1-28dd-478a-910e-a5dd2192c0c8">IFaxConfiguration::put_LowQuotaWaterMark</a>   or <a href="https://msdn.microsoft.com/939cf7c1-28dd-478a-910e-a5dd2192c0c8">IFaxConfiguration::get_LowQuotaWaterMark</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>
 

 

