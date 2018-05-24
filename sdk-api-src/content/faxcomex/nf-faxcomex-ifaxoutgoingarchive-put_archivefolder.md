---
UID: NF:faxcomex.IFaxOutgoingArchive.put_ArchiveFolder
title: IFaxOutgoingArchive::put_ArchiveFolder
author: windows-driver-content
description: The ArchiveFolder property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes.
old-location: fax\_mfax_faxoutgoingarchive_archivefolder_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4302.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ArchiveFolder property [Fax Service], ArchiveFolder property [Fax Service],FaxOutgoingArchive object, FaxOutgoingArchive object [Fax Service],ArchiveFolder property, FaxOutgoingArchive.ArchiveFolder, IFaxOutgoingArchive.put_ArchiveFolder, IFaxOutgoingArchive::put_ArchiveFolder, _mfax_faxoutgoingarchive.archivefolder, fax._mfax_faxoutgoingarchive_archivefolder, fax._mfax_faxoutgoingarchive_archivefolder_vb, put_ArchiveFolder
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxOutgoingArchive.ArchiveFolder
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingArchive::put_ArchiveFolder


## -description


The <b>ArchiveFolder</b> property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes.

This property is read-only.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows, get the  <a href="https://msdn.microsoft.com/42fb8a22-0404-404f-b761-c8b8783f98a3">FaxConfiguration.ArchiveLocation</a> property from the <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/381e098b-d130-4e15-9aba-cb0048cc5b98">FaxConfiguration</a>



<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/68f6c0f2-ea06-401c-9021-c50940f8cd7a">Visual Basic Example</a>
 

 

