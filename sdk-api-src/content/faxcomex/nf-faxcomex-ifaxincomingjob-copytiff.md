---
UID: NF:faxcomex.IFaxIncomingJob.CopyTiff
title: IFaxIncomingJob::CopyTiff
author: windows-sdk-content
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax job to a file on the local computer.
old-location: fax\_mfax_faxincomingjob_copytiff_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_136u.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],FaxIncomingJob object, FaxIncomingJob object [Fax Service],CopyTiff method, FaxIncomingJob.CopyTiff, IFaxIncomingJob.CopyTiff, IFaxIncomingJob::CopyTiff, _mfax_faxincomingjob.copytiff, fax._mfax_faxincomingjob_copytiff, fax._mfax_faxincomingjob_copytiff_vb
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxIncomingJob.CopyTiff
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingJob::CopyTiff


## -description


The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax job to a file on the local computer.


## -parameters




### -param bstrTiffPath [in]

Type: <b>String</b>

Null-terminated string that specifies a fully qualified path and file name on the local computer.


## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_JOBS</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>



<a href="https://msdn.microsoft.com/88cde2d4-09ee-4fbf-8a75-35de58dd45f5">Visual Basic Example</a>
 

 

