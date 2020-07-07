---
UID: NF:vswriter.CVssWriter.Unsubscribe
title: CVssWriter::Unsubscribe (vswriter.h)
description: The Unsubscribe method unsubscribes the writer with VSS.
helpviewer_keywords: ["CVssWriter interface [VSS]","Unsubscribe method","CVssWriter.Unsubscribe","CVssWriter::Unsubscribe","Unsubscribe","Unsubscribe method [VSS]","Unsubscribe method [VSS]","CVssWriter interface","_win32_cvsswriter_unsubscribe","base.cvsswriter_unsubscribe","vswriter/CVssWriter::Unsubscribe"]
old-location: base\cvsswriter_unsubscribe.htm
tech.root: VSS
ms.assetid: b2bb68d1-7beb-4ba1-b16d-6314ac3f4a3d
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],Unsubscribe method, CVssWriter.Unsubscribe, CVssWriter::Unsubscribe, Unsubscribe, Unsubscribe method [VSS], Unsubscribe method [VSS],CVssWriter interface, _win32_cvsswriter_unsubscribe, base.cvsswriter_unsubscribe, vswriter/CVssWriter::Unsubscribe
f1_keywords:
- vswriter/CVssWriter.Unsubscribe
dev_langs:
- c++
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- CVssWriter.Unsubscribe
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CVssWriter::Unsubscribe


## -description


The 
<b>Unsubscribe</b> method unsubscribes the writer with VSS.

<b>Unsubscribe</b> is a public method implemented by the 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.


## -parameters






## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully unsubscribed the writer object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>
 

 

