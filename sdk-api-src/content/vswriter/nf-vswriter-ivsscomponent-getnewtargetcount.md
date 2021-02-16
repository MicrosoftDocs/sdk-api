---
UID: NF:vswriter.IVssComponent.GetNewTargetCount
title: IVssComponent::GetNewTargetCount (vswriter.h)
description: The GetNewTargetCount method returns the number of new target restore locations associated with a given component.
helpviewer_keywords: ["GetNewTargetCount","GetNewTargetCount method [VSS]","GetNewTargetCount method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetNewTargetCount method","IVssComponent.GetNewTargetCount","IVssComponent::GetNewTargetCount","_win32_ivsscomponent_getnewtargetcount","base.ivsscomponent_getnewtargetcount","vswriter/IVssComponent::GetNewTargetCount"]
old-location: base\ivsscomponent_getnewtargetcount.htm
tech.root: base
ms.assetid: b41afed9-2689-469e-b3c4-83cf18c5f8a9
ms.date: 12/05/2018
ms.keywords: GetNewTargetCount, GetNewTargetCount method [VSS], GetNewTargetCount method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetNewTargetCount method, IVssComponent.GetNewTargetCount, IVssComponent::GetNewTargetCount, _win32_ivsscomponent_getnewtargetcount, base.ivsscomponent_getnewtargetcount, vswriter/IVssComponent::GetNewTargetCount
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
 - IVssComponent::GetNewTargetCount
 - vswriter/IVssComponent::GetNewTargetCount
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
 - IVssComponent.GetNewTargetCount
---

# IVssComponent::GetNewTargetCount


## -description

The 
<b>GetNewTargetCount</b> method returns the number of new target restore locations associated with a given component.

Either a writer or a requester can call this method.

## -parameters

### -param pcNewTarget [out]

The address of a caller-allocated variable that receives the number of new target restore locations.

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
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>