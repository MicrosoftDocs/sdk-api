---
UID: NF:vswriter.IVssComponent.SetRestoreTarget
title: IVssComponent::SetRestoreTarget (vswriter.h)
description: The SetRestoreTarget method sets the restore target (in terms of the VSS_RESTORE_TARGET enumeration) for the current component.
helpviewer_keywords: ["IVssComponent interface [VSS]","SetRestoreTarget method","IVssComponent.SetRestoreTarget","IVssComponent::SetRestoreTarget","SetRestoreTarget","SetRestoreTarget method [VSS]","SetRestoreTarget method [VSS]","IVssComponent interface","_win32_ivsscomponent_setrestoretarget","base.ivsscomponent_setrestoretarget","vswriter/IVssComponent::SetRestoreTarget"]
old-location: base\ivsscomponent_setrestoretarget.htm
tech.root: base
ms.assetid: 6e8b9322-6611-4a47-aa7a-876be01d33b8
ms.date: 12/05/2018
ms.keywords: IVssComponent interface [VSS],SetRestoreTarget method, IVssComponent.SetRestoreTarget, IVssComponent::SetRestoreTarget, SetRestoreTarget, SetRestoreTarget method [VSS], SetRestoreTarget method [VSS],IVssComponent interface, _win32_ivsscomponent_setrestoretarget, base.ivsscomponent_setrestoretarget, vswriter/IVssComponent::SetRestoreTarget
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
 - IVssComponent::SetRestoreTarget
 - vswriter/IVssComponent::SetRestoreTarget
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
 - IVssComponent.SetRestoreTarget
---

# IVssComponent::SetRestoreTarget


## -description

The 
<b>SetRestoreTarget</b> method sets the restore target (in terms of the 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restore_target">VSS_RESTORE_TARGET</a> enumeration) for the current component.

Only a writer can call this method, and only during a restore operation.

## -parameters

### -param target [in]

A value from 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restore_target">VSS_RESTORE_TARGET</a> containing the restore target information.

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
Successfully set the item.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The caller is not in the correct state (either backup or restore) for the operation.

</td>
</tr>
</table>

## -remarks

The restore target set by 
<b>SetRestoreTarget</b> applies to all files in the component and any nonselectable subcomponents.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>