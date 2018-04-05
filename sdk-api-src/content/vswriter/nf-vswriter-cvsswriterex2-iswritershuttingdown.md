---
UID: NF:vswriter.CVssWriterEx2.IsWriterShuttingDown
title: CVssWriterEx2::IsWriterShuttingDown method
author: windows-driver-content
description: Determines whether the writer is shutting down.
old-location: base\cvsswriterex2_iswritershuttingdown.htm
old-project: VSS
ms.assetid: 78ea5993-ee86-435b-a225-8cb6e5f1a240
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CVssWriterEx2, CVssWriterEx2 interface, IsWriterShuttingDown method, CVssWriterEx2::IsWriterShuttingDown, IsWriterShuttingDown method, IsWriterShuttingDown method, CVssWriterEx2 interface, IsWriterShuttingDown,CVssWriterEx2.IsWriterShuttingDown, base.cvsswriterex2_iswritershuttingdown, vswriter/CVssWriterEx2::IsWriterShuttingDown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	CVssWriterEx2.IsWriterShuttingDown
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriterEx2::IsWriterShuttingDown method


## -description


Determines whether the writer is shutting down.


## -parameters






## -returns



Returns <b>true</b> if the writer is shutting down, or <b>false</b> otherwise.




## -remarks



The writer implementation should call this method periodically during long-running events where the writer is performing a large amount of processing or looping. If this method returns <b>true</b> during the event, the writer should do the following:

<ol>
<li>Log an error to the Application Event Log event. This is optional, but recommended.</li>
<li>Call <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">SetWriterFailure</a> or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">SetWriterFailureEx</a>, passing a non-retryable error code for the <i>hr</i> or <i>hrWriter</i> parameter.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/13cdeae3-dece-42ae-8bff-037ee3e4cec4">CVssWriterEx2</a>
 

 

