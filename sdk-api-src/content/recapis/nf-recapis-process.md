---
UID: NF:recapis.Process
title: Process function (recapis.h)
description: Performs ink recognition synchronously.
helpviewer_keywords: ["564a2734-1a90-4566-a39d-7e16eff870ff","Process","Process function [Tablet PC]","recapis/Process","tablet.process"]
old-location: tablet\process.htm
tech.root: tablet
ms.assetid: 564a2734-1a90-4566-a39d-7e16eff870ff
ms.date: 12/05/2018
ms.keywords: 564a2734-1a90-4566-a39d-7e16eff870ff, Process, Process function [Tablet PC], recapis/Process, tablet.process
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Process
 - recapis/Process
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - Process
---

# Process function


## -description

Performs ink recognition synchronously.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param pbPartialProcessing

Specify <b>TRUE</b> to process a subset of the ink. Partial processing reduces the time the recognizer spends performing recognition if more ink is expected.

Typically an application specifies <b>FALSE</b> to process all the ink. The function does not process all the ink if you have not called the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput">EndInkInput</a> function.

The function sets the <i>pbPartialProcessing</i> parameter to <b>TRUE</b> if there is enough ink left to continue processing; otherwise, <b>FALSE</b>.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function did not process the ink because the ink has been fully processed, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput">EndInkInput</a> function has not been called and the recognizer does not support incremental processing of ink.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_S_INTERRUPTED</b></dt>
</dl>
</td>
<td width="60%">
The process was interrupted by a call to the <a href="/windows/desktop/api/recapis/nf-recapis-adviseinkchange">AdviseInkChange</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>