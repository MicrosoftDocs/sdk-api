---
UID: NF:faxcomex.IFaxIncomingArchive.get_ArchiveFolder
title: IFaxIncomingArchive::get_ArchiveFolder
author: windows-sdk-content
description: The ArchiveFolder property is a null-terminated string that specifies the folder location on the fax server for archived inbound faxes.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_archivefolder_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7vle.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ArchiveFolder property [Fax Service], ArchiveFolder property [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],ArchiveFolder property, IFaxIncomingArchive.ArchiveFolder, IFaxIncomingArchive.get_ArchiveFolder, IFaxIncomingArchive::ArchiveFolder, IFaxIncomingArchive::get_ArchiveFolder, IFaxIncomingArchive::put_ArchiveFolder, _mfax_faxincomingarchive.archivefolder, fax._mfax_faxincomingarchive_archivefolder, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_archivefolder_cpp, faxcomex/IFaxIncomingArchive::ArchiveFolder, faxcomex/IFaxIncomingArchive::get_ArchiveFolder, faxcomex/IFaxIncomingArchive::put_ArchiveFolder, get_ArchiveFolder
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
 - IFaxIncomingArchive.ArchiveFolder
 - IFaxIncomingArchive.get_ArchiveFolder
 - IFaxIncomingArchive.put_ArchiveFolder
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
- IFaxIncomingArchive.get_ArchiveFolder
: 
---

# IFaxIncomingArchive::get_ArchiveFolder


## -description


The <b>ArchiveFolder</b> property is a null-terminated string that specifies the folder location on the fax server for archived inbound faxes.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/c504b290-d970-4bc9-ae35-4b05b0d2be96">IFaxConfiguration::put_ArchiveLocation</a>   or <a href="https://msdn.microsoft.com/c504b290-d970-4bc9-ae35-4b05b0d2be96">IFaxConfiguration::get_ArchiveLocation</a> method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a81d6314-b26f-4946-896e-218a0095938f">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

