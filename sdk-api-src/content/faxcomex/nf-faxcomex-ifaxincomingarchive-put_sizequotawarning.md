---
UID: NF:faxcomex.IFaxIncomingArchive.put_SizeQuotaWarning
title: IFaxIncomingArchive::put_SizeQuotaWarning
author: windows-sdk-content
description: The SizeQuotaWarning property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the inbound archive exceeds the limit defined by the HighQuotaWaterMark property.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizequotawarning_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3t5z.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],SizeQuotaWarning property, IFaxIncomingArchive.SizeQuotaWarning, IFaxIncomingArchive.get_SizeQuotaWarning, IFaxIncomingArchive.put_SizeQuotaWarning, IFaxIncomingArchive::SizeQuotaWarning, IFaxIncomingArchive::get_SizeQuotaWarning, IFaxIncomingArchive::put_SizeQuotaWarning, SizeQuotaWarning property [Fax Service], SizeQuotaWarning property [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.sizequotawarning, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_sizequotawarning_cpp, fax._mfax_faxincomingarchive_sizequotawarning, faxcomex/IFaxIncomingArchive::SizeQuotaWarning, faxcomex/IFaxIncomingArchive::get_SizeQuotaWarning, faxcomex/IFaxIncomingArchive::put_SizeQuotaWarning, put_SizeQuotaWarning
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
 - IFaxIncomingArchive.SizeQuotaWarning
 - IFaxIncomingArchive.get_SizeQuotaWarning
 - IFaxIncomingArchive.put_SizeQuotaWarning
 - IFaxIncomingArchive.get_SizeQuotaWarning
 - IFaxIncomingArchive.put_SizeQuotaWarning
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxIncomingArchive.put_SizeQuotaWarning
: 
---

# IFaxIncomingArchive::put_SizeQuotaWarning


## -description


The <b>SizeQuotaWarning</b> property is a Boolean value that indicates whether the fax service issues a warning in the event log when the size of the inbound archive exceeds the limit defined by the <a href="https://msdn.microsoft.com/aa03892c-efa9-421f-9223-e83b3dba7b12">HighQuotaWaterMark</a> property.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/541abd86-8edb-4d52-a323-5bdafab24653">IFaxConfiguration::put_SizeQuotaWarning</a>   or <a href="https://msdn.microsoft.com/541abd86-8edb-4d52-a323-5bdafab24653">IFaxConfiguration::get_SizeQuotaWarning</a> method.</div>
<div> </div>
If this property is equal to <b>TRUE</b>, the fax service will issue a warning when the number of fax messages exceeds the threshold. If this property is equal to <b>FALSE</b>, the fax service does not issue a warning.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/a81d6314-b26f-4946-896e-218a0095938f">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

