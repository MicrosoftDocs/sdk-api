---
UID: NF:vswriter.IVssComponent.GetComponentType
title: IVssComponent::GetComponentType (vswriter.h)
description: The GetComponentType method returns the type of this component in terms of the VSS_COMPONENT_TYPE enumeration.
helpviewer_keywords: ["GetComponentType","GetComponentType method [VSS]","GetComponentType method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetComponentType method","IVssComponent.GetComponentType","IVssComponent::GetComponentType","_win32_ivsscomponent_getcomponenttype","base.ivsscomponent_getcomponenttype","vswriter/IVssComponent::GetComponentType"]
old-location: base\ivsscomponent_getcomponenttype.htm
tech.root: base
ms.assetid: 89675df6-dcfd-4167-aa6f-5c88e619ef1c
ms.date: 12/05/2018
ms.keywords: GetComponentType, GetComponentType method [VSS], GetComponentType method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetComponentType method, IVssComponent.GetComponentType, IVssComponent::GetComponentType, _win32_ivsscomponent_getcomponenttype, base.ivsscomponent_getcomponenttype, vswriter/IVssComponent::GetComponentType
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
 - IVssComponent::GetComponentType
 - vswriter/IVssComponent::GetComponentType
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
 - IVssComponent.GetComponentType
---

# IVssComponent::GetComponentType


## -description

The 
<b>GetComponentType</b> method returns the type of this component in terms of the 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> enumeration.

Either a writer or a requester can call this method.

## -parameters

### -param pct [out]

The address of a caller-allocated variable that receives a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> enumeration value that specifies the type of the component.

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
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>