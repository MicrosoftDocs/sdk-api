---
UID: NF:vswriter.IVssComponent.GetDirectedTargetCount
title: IVssComponent::GetDirectedTargetCount (vswriter.h)
description: The GetDirectedTargetCount method returns the number of directed target specifications associated with the current component. Either a writer or a requester can call this method.
helpviewer_keywords: ["GetDirectedTargetCount","GetDirectedTargetCount method [VSS]","GetDirectedTargetCount method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetDirectedTargetCount method","IVssComponent.GetDirectedTargetCount","IVssComponent::GetDirectedTargetCount","_win32_ivsscomponent_getdirectedtargetcount","base.ivsscomponent_getdirectedtargetcount","vswriter/IVssComponent::GetDirectedTargetCount"]
old-location: base\ivsscomponent_getdirectedtargetcount.htm
tech.root: base
ms.assetid: 3c8cf80e-66b9-4c6f-a63d-90626937582b
ms.date: 12/05/2018
ms.keywords: GetDirectedTargetCount, GetDirectedTargetCount method [VSS], GetDirectedTargetCount method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetDirectedTargetCount method, IVssComponent.GetDirectedTargetCount, IVssComponent::GetDirectedTargetCount, _win32_ivsscomponent_getdirectedtargetcount, base.ivsscomponent_getdirectedtargetcount, vswriter/IVssComponent::GetDirectedTargetCount
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
 - IVssComponent::GetDirectedTargetCount
 - vswriter/IVssComponent::GetDirectedTargetCount
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
 - IVssComponent.GetDirectedTargetCount
---

# IVssComponent::GetDirectedTargetCount


## -description

The 
<b>GetDirectedTargetCount</b> method returns the number of directed target specifications associated with the current component. Either a writer or a requester can call this method.

## -parameters

### -param pcDirectedTarget [out]

The address of a caller-allocated variable that receives the number of directed target specifications.

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



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddirectedtarget">IVssComponent::AddDirectedTarget</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdirectedtarget">IVssComponent::GetDirectedTarget</a>