---
UID: NF:vswriter.IVssComponent.GetComponentName
title: IVssComponent::GetComponentName (vswriter.h)
description: The GetComponentName method returns the logical name of this component.
helpviewer_keywords: ["GetComponentName","GetComponentName method [VSS]","GetComponentName method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetComponentName method","IVssComponent.GetComponentName","IVssComponent::GetComponentName","_win32_ivsscomponent_getcomponentname","base.ivsscomponent_getcomponentname","vswriter/IVssComponent::GetComponentName"]
old-location: base\ivsscomponent_getcomponentname.htm
tech.root: base
ms.assetid: 24b36ea6-3662-4846-a90b-5c2da578e1fa
ms.date: 12/05/2018
ms.keywords: GetComponentName, GetComponentName method [VSS], GetComponentName method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetComponentName method, IVssComponent.GetComponentName, IVssComponent::GetComponentName, _win32_ivsscomponent_getcomponentname, base.ivsscomponent_getcomponentname, vswriter/IVssComponent::GetComponentName
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
 - IVssComponent::GetComponentName
 - vswriter/IVssComponent::GetComponentName
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
 - IVssComponent.GetComponentName
---

# IVssComponent::GetComponentName


## -description

The 
<b>GetComponentName</b> method returns the logical name of this component.

Either a writer or a requester can call this method.

## -parameters

### -param pbstrName [out]

Pointer to a string containing the logical name of the component.

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
This component has no name. This state should never occur.

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

The caller should free the memory held by the <i>pwszName</i> parameter by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>