---
UID: NF:faxcomex.IFaxOutgoingArchive.put_SizeQuotaWarning
title: IFaxOutgoingArchive::put_SizeQuotaWarning
author: windows-sdk-content
description: The IFaxOutgoingArchive::get_SizeQuotaWarning property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the outbound archive exceeds the limit defined by the IFaxOutgoingArchive::get_HighQuotaWaterMark property.
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizequotawarning_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6wkn.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],SizeQuotaWarning property, IFaxOutgoingArchive.SizeQuotaWarning, IFaxOutgoingArchive.get_SizeQuotaWarning, IFaxOutgoingArchive.put_SizeQuotaWarning, IFaxOutgoingArchive::SizeQuotaWarning, IFaxOutgoingArchive::get_SizeQuotaWarning, IFaxOutgoingArchive::put_SizeQuotaWarning, SizeQuotaWarning property [Fax Service], SizeQuotaWarning property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.sizequotawarning, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizequotawarning_cpp, fax._mfax_faxoutgoingarchive_sizequotawarning, faxcomex/IFaxOutgoingArchive::SizeQuotaWarning, faxcomex/IFaxOutgoingArchive::get_SizeQuotaWarning, faxcomex/IFaxOutgoingArchive::put_SizeQuotaWarning, put_SizeQuotaWarning
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
 - IFaxOutgoingArchive.SizeQuotaWarning
 - IFaxOutgoingArchive.get_SizeQuotaWarning
 - IFaxOutgoingArchive.put_SizeQuotaWarning
 - IFaxOutgoingArchive.get_SizeQuotaWarning
 - IFaxOutgoingArchive.put_SizeQuotaWarning
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingArchive::put_SizeQuotaWarning


## -description


The <b>IFaxOutgoingArchive::get_SizeQuotaWarning</b> property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the outbound archive exceeds the limit defined by the <a href="https://msdn.microsoft.com/d89daf43-810a-4539-9ad6-5f6476660755">IFaxOutgoingArchive::get_HighQuotaWaterMark</a> property.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/541abd86-8edb-4d52-a323-5bdafab24653">IFaxConfiguration::put_SizeQuotaWarning</a>   or <a href="https://msdn.microsoft.com/541abd86-8edb-4d52-a323-5bdafab24653">IFaxConfiguration::get_SizeQuotaWarning</a> method.</div>
<div> </div>
If this property is equal to <b>TRUE</b>, the fax service issues a warning when the number of fax messages in the archive exceeds the limit. If this property is equal to <b>FALSE</b>, the fax service does not issue a warning.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>
 

 

