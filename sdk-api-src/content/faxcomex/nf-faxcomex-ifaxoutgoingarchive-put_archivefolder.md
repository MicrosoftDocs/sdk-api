---
UID: NF:faxcomex.IFaxOutgoingArchive.put_ArchiveFolder
title: IFaxOutgoingArchive::put_ArchiveFolder
author: windows-sdk-content
description: The IFaxOutgoingArchive::get_ArchiveFolder property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes.
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_archivefolder_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4302.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ArchiveFolder property [Fax Service], ArchiveFolder property [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],ArchiveFolder property, IFaxOutgoingArchive.ArchiveFolder, IFaxOutgoingArchive.put_ArchiveFolder, IFaxOutgoingArchive::ArchiveFolder, IFaxOutgoingArchive::get_ArchiveFolder, IFaxOutgoingArchive::put_ArchiveFolder, _mfax_faxoutgoingarchive.archivefolder, fax._mfax_faxoutgoingarchive_archivefolder, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_archivefolder_cpp, faxcomex/IFaxOutgoingArchive::ArchiveFolder, faxcomex/IFaxOutgoingArchive::get_ArchiveFolder, faxcomex/IFaxOutgoingArchive::put_ArchiveFolder, put_ArchiveFolder
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
 - IFaxOutgoingArchive.ArchiveFolder
 - IFaxOutgoingArchive.get_ArchiveFolder
 - IFaxOutgoingArchive.put_ArchiveFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingArchive::put_ArchiveFolder


## -description


The <b>IFaxOutgoingArchive::get_ArchiveFolder</b> property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/c504b290-d970-4bc9-ae35-4b05b0d2be96">IFaxConfiguration::put_ArchiveLocation</a>   or <a href="https://msdn.microsoft.com/c504b290-d970-4bc9-ae35-4b05b0d2be96">IFaxConfiguration::get_ArchiveLocation</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/68f6c0f2-ea06-401c-9021-c50940f8cd7a">Visual Basic Example</a>
 

 

