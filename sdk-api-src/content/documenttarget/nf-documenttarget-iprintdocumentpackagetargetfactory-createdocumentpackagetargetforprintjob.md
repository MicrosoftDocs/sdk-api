---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob


## -description


Acts as the entry point for creating an <a href="https://msdn.microsoft.com/0F63C626-DB58-4952-BBB3-7E3901429C35">IPrintDocumentPackageTarget</a> object.


## -parameters




### -param printerName [in]

The name of the target printer.


### -param jobName [in]

The name to apply to the job.

<div class="alert"><b>Note</b>  Job name strings longer than 63 characters will be truncated to 63 characters and a terminating <b>NULL</b>.</div>
<div> </div>

### -param jobOutputStream [in]

The job content. The application must set the seek pointer to the beginning before specifying the job output stream.


### -param jobPrintTicketStream [in]

A pointer to the <b>IStream</b> interface that is used by the caller to write the job-level print ticket that will be associated with this job.


### -param docPackageTarget [out]

The target output.


## -returns



If the <b>CreateDocumentPackageTargetForPrintJob</b> method completes successfully, it returns an S_OK. Otherwise it returns the appropriate HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/0F63C626-DB58-4952-BBB3-7E3901429C35">IPrintDocumentPackageTarget</a>



<a href="https://msdn.microsoft.com/631FBF5E-1DDF-49A9-8E1E-201BC6996EA5">IPrintDocumentPackageTargetFactory</a>
 

 

