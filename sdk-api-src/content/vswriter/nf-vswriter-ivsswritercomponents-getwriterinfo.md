---
UID: NF:vswriter.IVssWriterComponents.GetWriterInfo
title: IVssWriterComponents::GetWriterInfo (vswriter.h)
description: The GetWriterInfo method gets the instance and class identifier of the writer responsible for the components.
helpviewer_keywords: ["GetWriterInfo","GetWriterInfo method [VSS]","GetWriterInfo method [VSS]","IVssWriterComponents interface","IVssWriterComponents interface [VSS]","GetWriterInfo method","IVssWriterComponents.GetWriterInfo","IVssWriterComponents::GetWriterInfo","_win32_ivsswritercomponents_getwriterinfo","base.ivsswritercomponents_getwriterinfo","vswriter/IVssWriterComponents::GetWriterInfo"]
old-location: base\ivsswritercomponents_getwriterinfo.htm
tech.root: base
ms.assetid: 22a539ac-1440-4fe9-b68e-feec97cab6c8
ms.date: 12/05/2018
ms.keywords: GetWriterInfo, GetWriterInfo method [VSS], GetWriterInfo method [VSS],IVssWriterComponents interface, IVssWriterComponents interface [VSS],GetWriterInfo method, IVssWriterComponents.GetWriterInfo, IVssWriterComponents::GetWriterInfo, _win32_ivsswritercomponents_getwriterinfo, base.ivsswritercomponents_getwriterinfo, vswriter/IVssWriterComponents::GetWriterInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssWriterComponents::GetWriterInfo
 - vswriter/IVssWriterComponents::GetWriterInfo
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
 - IVssWriterComponents.GetWriterInfo
---

# IVssWriterComponents::GetWriterInfo


## -description

The 
<b>GetWriterInfo</b> method gets the instance and class identifier of the writer responsible for the components.

## -parameters

### -param pidInstance [out]

Identifier of the writer instance.

### -param pidWriter [out]

Identifier of the writer class.

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
Successfully returned the component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

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
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a>