---
UID: NF:vswriter.IVssComponent.GetRestoreSubcomponent
title: IVssComponent::GetRestoreSubcomponent (vswriter.h)
description: The GetRestoreSubcomponent method returns the specified subcomponent associated with a given component.
helpviewer_keywords: ["GetRestoreSubcomponent","GetRestoreSubcomponent method [VSS]","GetRestoreSubcomponent method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetRestoreSubcomponent method","IVssComponent.GetRestoreSubcomponent","IVssComponent::GetRestoreSubcomponent","_win32_ivsscomponent_getrestoresubcomponent","base.ivsscomponent_getrestoresubcomponent","vswriter/IVssComponent::GetRestoreSubcomponent"]
old-location: base\ivsscomponent_getrestoresubcomponent.htm
tech.root: base
ms.assetid: 23c37342-fcbd-4401-83d5-a52d4a69b908
ms.date: 12/05/2018
ms.keywords: GetRestoreSubcomponent, GetRestoreSubcomponent method [VSS], GetRestoreSubcomponent method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetRestoreSubcomponent method, IVssComponent.GetRestoreSubcomponent, IVssComponent::GetRestoreSubcomponent, _win32_ivsscomponent_getrestoresubcomponent, base.ivsscomponent_getrestoresubcomponent, vswriter/IVssComponent::GetRestoreSubcomponent
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
 - IVssComponent::GetRestoreSubcomponent
 - vswriter/IVssComponent::GetRestoreSubcomponent
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
 - IVssComponent.GetRestoreSubcomponent
---

# IVssComponent::GetRestoreSubcomponent


## -description

The 
<b>GetRestoreSubcomponent</b> method returns the specified subcomponent associated with a given component.

Either a writer or a requester can call this method.

## -parameters

### -param iComponent [in]

Index of the subcomponent. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of subcomponents associated with a given component. The value of <i>n</i> is returned by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount">IVssComponent::GetRestoreSubcomponentCount</a>.

### -param pbstrLogicalPath [out]

Pointer to a string containing the logical path of the subcomponent. The logical path cannot be empty when working with subcomponents.

### -param pbstrComponentName [out]

Pointer to a string containing the name of the subcomponent. The string cannot be empty.

### -param pbRepair [out]

Reserved for future use.

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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified item was not found.

</td>
</tr>
</table>

## -remarks

The caller should free the memory held by the <i>pbstrLogicalPath</i> and <i>pbstrComponentName</i> parameters by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>