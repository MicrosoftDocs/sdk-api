---
UID: NF:faxcomex.IFaxOutgoingArchive.put_ArchiveFolder
title: IFaxOutgoingArchive::put_ArchiveFolder
author: windows-sdk-content
description: The ArchiveFolder property is a null-terminated string that specifies the folder location on the fax server for archived outbound faxes.
old-location: fax\_mfax_faxoutgoingarchive_archivefolder_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4302.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ArchiveFolder property [Fax Service], ArchiveFolder property [Fax Service],FaxOutgoingArchive object, FaxOutgoingArchive object [Fax Service],ArchiveFolder property, FaxOutgoingArchive.ArchiveFolder, IFaxOutgoingArchive.put_ArchiveFolder, IFaxOutgoingArchive::put_ArchiveFolder, _mfax_faxoutgoingarchive.archivefolder, fax._mfax_faxoutgoingarchive_archivefolder, fax._mfax_faxoutgoingarchive_archivefolder_vb, put_ArchiveFolder
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutgoingArchive.ArchiveFolder
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



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows, get the  <a href="https://msdn.microsoft.com/en-us/library/Aa358915(v=VS.85).aspx">FaxConfiguration.ArchiveLocation</a> property from the <a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a> object.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa358913(v=VS.85).aspx">FaxConfiguration</a>



<a href="https://msdn.microsoft.com/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/library/ms688636(v=VS.85).aspx">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/library/ms693472(v=VS.85).aspx">Visual Basic Example</a>
 

 

