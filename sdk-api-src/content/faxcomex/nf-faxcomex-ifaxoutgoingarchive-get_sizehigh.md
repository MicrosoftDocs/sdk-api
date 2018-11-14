---
UID: NF:faxcomex.IFaxOutgoingArchive.get_SizeHigh
title: IFaxOutgoingArchive::get_SizeHigh
author: windows-sdk-content
description: The IFaxOutgoingArchive::get_SizeHigh property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of outgoing fax messages.
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizehigh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4je0.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],SizeHigh property, IFaxOutgoingArchive.SizeHigh, IFaxOutgoingArchive.get_SizeHigh, IFaxOutgoingArchive::SizeHigh, IFaxOutgoingArchive::get_SizeHigh, SizeHigh property [Fax Service], SizeHigh property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.sizehigh, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_sizehigh_cpp, fax._mfax_faxoutgoingarchive_sizehigh, faxcomex/IFaxOutgoingArchive::SizeHigh, faxcomex/IFaxOutgoingArchive::get_SizeHigh, get_SizeHigh
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
 - IFaxOutgoingArchive.SizeHigh
 - IFaxOutgoingArchive.get_SizeHigh
 - IFaxOutgoingArchive.get_SizeHigh
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
- IFaxOutgoingArchive.get_SizeHigh
: 
---

# IFaxOutgoingArchive::get_SizeHigh


## -description


The <b>IFaxOutgoingArchive::get_SizeHigh</b> property is a value that specifies the high 32-bit value (in bytes) for the size of the archive of outgoing fax messages.

This property is read-only.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/3386ec80-be4e-4105-ab57-dd634b57f67f">IFaxConfiguration::get_ArchiveSizeHigh</a> method.</div>
<div> </div>
Because the archive may exceed 4 gigabytes (GB) in size, the archive size is described using two long values. <a href="https://msdn.microsoft.com/045cfc9f-7385-48fb-834b-1ccad331bd37">SizeLow</a> is the low 32-bit value of the archive size. <b>SizeHigh</b> is the high 32-bit value of the archive size. The size of the archive is: <b>SizeLow</b> + 4 GB * <b>SizeHigh</b>. If both the <b>SizeLow</b> and <b>SizeHigh</b> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/68f6c0f2-ea06-401c-9021-c50940f8cd7a">Visual Basic Example</a>
 

 

