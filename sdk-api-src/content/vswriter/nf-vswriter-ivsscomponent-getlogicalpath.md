---
UID: NF:vswriter.IVssComponent.GetLogicalPath
title: IVssComponent::GetLogicalPath (vswriter.h)
description: The GetLogicalPath method returns the logical path of this component.
helpviewer_keywords: ["GetLogicalPath","GetLogicalPath method [VSS]","GetLogicalPath method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetLogicalPath method","IVssComponent.GetLogicalPath","IVssComponent::GetLogicalPath","_win32_ivsscomponent_getlogicalpath","base.ivsscomponent_getlogicalpath","vswriter/IVssComponent::GetLogicalPath"]
old-location: base\ivsscomponent_getlogicalpath.htm
tech.root: base
ms.assetid: 16c85322-5127-40aa-8393-df7684cd1c92
ms.date: 12/05/2018
ms.keywords: GetLogicalPath, GetLogicalPath method [VSS], GetLogicalPath method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetLogicalPath method, IVssComponent.GetLogicalPath, IVssComponent::GetLogicalPath, _win32_ivsscomponent_getlogicalpath, base.ivsscomponent_getlogicalpath, vswriter/IVssComponent::GetLogicalPath
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
 - IVssComponent::GetLogicalPath
 - vswriter/IVssComponent::GetLogicalPath
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
 - IVssComponent.GetLogicalPath
---

# IVssComponent::GetLogicalPath


## -description

The 
<b>GetLogicalPath</b> method returns the logical path of this component.

Either a writer or a requester can call this method.

## -parameters

### -param pbstrPath [out]

Pointer to a string containing the logical path of the component.

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
Successfully returned the attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This component has no logical path.

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

## -remarks

The caller should free the memory held by the <i>pbstrPath</i> parameter by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

Logical paths are not required of components. A component without a logical path will return S_FALSE.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>