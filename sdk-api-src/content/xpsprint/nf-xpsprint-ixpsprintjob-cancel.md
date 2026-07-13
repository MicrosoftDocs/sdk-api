---
UID: NF:xpsprint.IXpsPrintJob.Cancel
title: IXpsPrintJob::Cancel (xpsprint.h)
description: Cancels the print job.
helpviewer_keywords: ["Cancel","Cancel method [Windows GDI]","Cancel method [Windows GDI]","IXpsPrintJob interface","IXpsPrintJob interface [Windows GDI]","Cancel method","IXpsPrintJob.Cancel","IXpsPrintJob::Cancel","gdi.ixpsprintjob_cancel","xpsprint/IXpsPrintJob::Cancel"]
old-location: gdi\ixpsprintjob_cancel.htm
tech.root: xps
ms.assetid: f9fab578-95f0-498b-85ad-fd6ee2c72c63
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows GDI], Cancel method [Windows GDI],IXpsPrintJob interface, IXpsPrintJob interface [Windows GDI],Cancel method, IXpsPrintJob.Cancel, IXpsPrintJob::Cancel, gdi.ixpsprintjob_cancel, xpsprint/IXpsPrintJob::Cancel
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IXpsPrintJob::Cancel
 - xpsprint/IXpsPrintJob::Cancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsPrint.h
api_name:
 - IXpsPrintJob.Cancel
---

# IXpsPrintJob::Cancel


## -description

<p class="CCE_Message">[IXpsPrintJob::Cancel is not supported and may be altered or unavailable in the future. ]

Cancels the print job.



## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Any spooling or printing that is in progress at the time this method is called will be canceled.

This function is thread-safe and synchronized with the job status of the print job object.

## -see-also

<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjob">IXpsPrintJob</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
