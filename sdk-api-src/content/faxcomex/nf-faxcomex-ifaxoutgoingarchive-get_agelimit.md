---
UID: NF:faxcomex.IFaxOutgoingArchive.get_AgeLimit
title: IFaxOutgoingArchive::get_AgeLimit
author: windows-sdk-content
description: The IFaxOutgoingArchive::get_AgeLimit property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes.
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_agelimit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_69mc.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],AgeLimit property, IFaxOutgoingArchive.AgeLimit, IFaxOutgoingArchive.get_AgeLimit, IFaxOutgoingArchive::AgeLimit, IFaxOutgoingArchive::get_AgeLimit, IFaxOutgoingArchive::put_AgeLimit, _mfax_faxoutgoingarchive.agelimit, fax._mfax_faxoutgoingarchive_agelimit, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_agelimit_cpp, faxcomex/IFaxOutgoingArchive::AgeLimit, faxcomex/IFaxOutgoingArchive::get_AgeLimit, faxcomex/IFaxOutgoingArchive::put_AgeLimit, get_AgeLimit
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
 - IFaxOutgoingArchive.AgeLimit
 - IFaxOutgoingArchive.get_AgeLimit
 - IFaxOutgoingArchive.put_AgeLimit
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
- IFaxOutgoingArchive.get_AgeLimit
: 
---

# IFaxOutgoingArchive::get_AgeLimit


## -description


The <b>IFaxOutgoingArchive::get_AgeLimit</b> property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes. The fax service deletes messages from the outbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/2672f0e3-e412-4263-b3d1-b5b6c9cae708">IFaxConfiguration::put_ArchiveAgeLimit</a>   or <a href="https://msdn.microsoft.com/2672f0e3-e412-4263-b3d1-b5b6c9cae708">IFaxConfiguration::get_ArchiveAgeLimit</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/68f6c0f2-ea06-401c-9021-c50940f8cd7a">Visual Basic Example</a>
 

 

