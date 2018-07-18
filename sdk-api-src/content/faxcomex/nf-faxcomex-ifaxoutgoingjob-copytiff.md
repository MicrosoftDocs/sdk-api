---
UID: NF:faxcomex.IFaxOutgoingJob.CopyTiff
title: IFaxOutgoingJob::CopyTiff
author: windows-sdk-content
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax job, to a file on the local computer.
old-location: fax\_mfax_faxoutgoingjob_copytiff_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8mli.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],FaxOutgoingJob object, FaxOutgoingJob object [Fax Service],CopyTiff method, FaxOutgoingJob.CopyTiff, IFaxOutgoingJob.CopyTiff, IFaxOutgoingJob::CopyTiff, _mfax_faxoutgoingjob.copytiff, fax._mfax_faxoutgoingjob_copytiff, fax._mfax_faxoutgoingjob_copytiff_vb
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
 - FaxOutgoingJob.CopyTiff
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingJob::CopyTiff


## -description


The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the outbound fax job, to a file on the local computer.


## -parameters




### -param bstrTiffPath

Type: <b>String</b>

Null-terminated string that contains a fully qualified path and file name on the local computer. The fax service will copy the TIFF Class F file associated with the outbound fax to the specified file.


## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <b>farQUERY_JOBS</b> access right.

With the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farQUERY_JOBS</b> access right, users will be able to use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/library/ms689116(v=VS.85).aspx">IFaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/library/ms693393(v=VS.85).aspx">Visual Basic Example</a>
 

 

