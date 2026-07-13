---
UID: NF:vswriter.CVssWriterEx2.IsWriterShuttingDown
title: CVssWriterEx2::IsWriterShuttingDown (vswriter.h)
description: Determines whether the writer is shutting down.
helpviewer_keywords: ["CVssWriterEx2 interface","IsWriterShuttingDown method","CVssWriterEx2.IsWriterShuttingDown","CVssWriterEx2::IsWriterShuttingDown","IsWriterShuttingDown","IsWriterShuttingDown method","IsWriterShuttingDown method","CVssWriterEx2 interface","base.cvsswriterex2_iswritershuttingdown","vswriter/CVssWriterEx2::IsWriterShuttingDown"]
old-location: base\cvsswriterex2_iswritershuttingdown.htm
tech.root: base
ms.assetid: 78ea5993-ee86-435b-a225-8cb6e5f1a240
ms.date: 12/05/2018
ms.keywords: CVssWriterEx2 interface,IsWriterShuttingDown method, CVssWriterEx2.IsWriterShuttingDown, CVssWriterEx2::IsWriterShuttingDown, IsWriterShuttingDown, IsWriterShuttingDown method, IsWriterShuttingDown method,CVssWriterEx2 interface, base.cvsswriterex2_iswritershuttingdown, vswriter/CVssWriterEx2::IsWriterShuttingDown
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriterEx2::IsWriterShuttingDown
 - vswriter/CVssWriterEx2::IsWriterShuttingDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriterEx2.IsWriterShuttingDown
---

# CVssWriterEx2::IsWriterShuttingDown


## -description

Determines whether the writer is shutting down.



## -returns

Returns <b>true</b> if the writer is shutting down, or <b>false</b> otherwise.

## -remarks

The writer implementation should call this method periodically during long-running events where the writer is performing a large amount of processing or looping. If this method returns <b>true</b> during the event, the writer should do the following:

<ol>
<li>Log an error to the Application Event Log event. This is optional, but recommended.</li>
<li>Call <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">SetWriterFailure</a> or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">SetWriterFailureEx</a>, passing a non-retryable error code for the <i>hr</i> or <i>hrWriter</i> parameter.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex2">CVssWriterEx2</a>
