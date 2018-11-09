---
UID: NF:faxcomex.IFaxIncomingArchive.get_AgeLimit
title: IFaxIncomingArchive::get_AgeLimit
author: windows-sdk-content
description: The AgeLimit property is a value that indicates the number of days that the fax service retains fax messages in the archive of inbound faxes.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_agelimit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6vjo.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],AgeLimit property, IFaxIncomingArchive.AgeLimit, IFaxIncomingArchive.get_AgeLimit, IFaxIncomingArchive::AgeLimit, IFaxIncomingArchive::get_AgeLimit, IFaxIncomingArchive::put_AgeLimit, _mfax_faxincomingarchive.agelimit, fax._mfax_faxincomingarchive_agelimit, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_agelimit_cpp, faxcomex/IFaxIncomingArchive::AgeLimit, faxcomex/IFaxIncomingArchive::get_AgeLimit, faxcomex/IFaxIncomingArchive::put_AgeLimit, get_AgeLimit
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
 - IFaxIncomingArchive.AgeLimit
 - IFaxIncomingArchive.get_AgeLimit
 - IFaxIncomingArchive.put_AgeLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingArchive::get_AgeLimit


## -description


The <b>AgeLimit</b> property is a value that indicates the number of days that the fax service retains fax messages in the archive of inbound faxes. The fax service deletes messages from the inbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/2672f0e3-e412-4263-b3d1-b5b6c9cae708">IFaxConfiguration::put_ArchiveAgeLimit</a>   or <a href="https://msdn.microsoft.com/2672f0e3-e412-4263-b3d1-b5b6c9cae708">IFaxConfiguration::get_ArchiveAgeLimit</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/a81d6314-b26f-4946-896e-218a0095938f">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

