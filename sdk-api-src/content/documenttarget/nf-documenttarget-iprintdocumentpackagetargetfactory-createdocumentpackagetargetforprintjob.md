---
UID: NF:documenttarget.IPrintDocumentPackageTargetFactory.CreateDocumentPackageTargetForPrintJob
title: IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob (documenttarget.h)
description: Acts as the entry point for creating an IPrintDocumentPackageTarget object.
helpviewer_keywords: ["CreateDocumentPackageTargetForPrintJob","CreateDocumentPackageTargetForPrintJob method [XPS Documents and Packaging]","CreateDocumentPackageTargetForPrintJob method [XPS Documents and Packaging]","IPrintDocumentPackageTargetFactory interface","IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging]","CreateDocumentPackageTargetForPrintJob method","IPrintDocumentPackageTargetFactory.CreateDocumentPackageTargetForPrintJob","IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob","documenttarget/IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob","xps.iprintdocumentpackagetargetfactory_createdocumentpackagetargetforprintjob"]
old-location: xps\iprintdocumentpackagetargetfactory_createdocumentpackagetargetforprintjob.htm
tech.root: xps
ms.assetid: F611305F-B577-403F-AD8A-402ABE8F6768
ms.date: 12/05/2018
ms.keywords: CreateDocumentPackageTargetForPrintJob, CreateDocumentPackageTargetForPrintJob method [XPS Documents and Packaging], CreateDocumentPackageTargetForPrintJob method [XPS Documents and Packaging],IPrintDocumentPackageTargetFactory interface, IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging],CreateDocumentPackageTargetForPrintJob method, IPrintDocumentPackageTargetFactory.CreateDocumentPackageTargetForPrintJob, IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob, documenttarget/IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob, xps.iprintdocumentpackagetargetfactory_createdocumentpackagetargetforprintjob
req.header: documenttarget.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob
 - documenttarget/IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Documenttarget.h
api_name:
 - IPrintDocumentPackageTargetFactory.CreateDocumentPackageTargetForPrintJob
---

# IPrintDocumentPackageTargetFactory::CreateDocumentPackageTargetForPrintJob


## -description

Acts as the entry point for creating an <a href="/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget">IPrintDocumentPackageTarget</a> object.

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

<a href="/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget">IPrintDocumentPackageTarget</a>



<a href="/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory">IPrintDocumentPackageTargetFactory</a>