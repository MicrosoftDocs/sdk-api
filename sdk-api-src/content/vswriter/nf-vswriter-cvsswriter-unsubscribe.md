---
UID: NF:vswriter.CVssWriter.Unsubscribe
title: CVssWriter::Unsubscribe
author: windows-sdk-content
description: The Unsubscribe method unsubscribes the writer with VSS.
old-location: base\cvsswriter_unsubscribe.htm
tech.root: VSS
ms.assetid: b2bb68d1-7beb-4ba1-b16d-6314ac3f4a3d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CVssWriter interface [VSS],Unsubscribe method, CVssWriter.Unsubscribe, CVssWriter::Unsubscribe, Unsubscribe, Unsubscribe method [VSS], Unsubscribe method [VSS],CVssWriter interface, _win32_cvsswriter_unsubscribe, base.cvsswriter_unsubscribe, vswriter/CVssWriter::Unsubscribe
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriter::Unsubscribe


## -description


The 
<b>Unsubscribe</b> method unsubscribes the writer with VSS.

<b>Unsubscribe</b> is a public method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>
 

 

