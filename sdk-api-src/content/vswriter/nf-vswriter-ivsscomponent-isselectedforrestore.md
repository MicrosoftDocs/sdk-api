---
UID: NF:vswriter.IVssComponent.IsSelectedForRestore
title: IVssComponent::IsSelectedForRestore
author: windows-sdk-content
description: The IsSelectedForRestore method determines whether the current component has been selected to be restored.
old-location: base\ivsscomponent_isselectedforrestore.htm
old-project: VSS
ms.assetid: 76d0461d-a0ac-49c7-84b1-16f21114b72d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssComponent interface [VSS],IsSelectedForRestore method, IVssComponent.IsSelectedForRestore, IVssComponent::IsSelectedForRestore, IsSelectedForRestore, IsSelectedForRestore method [VSS], IsSelectedForRestore method [VSS],IVssComponent interface, _win32_ivsscomponent_isselectedforrestore, base.ivsscomponent_isselectedforrestore, vswriter/IVssComponent::IsSelectedForRestore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.redist: 
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponent.IsSelectedForRestore
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::IsSelectedForRestore


## -description


The 
<b>IsSelectedForRestore</b> method determines whether the current component has been selected to be restored.

Either a writer or a requester can call this method.


## -parameters




### -param pbSelectedForRestore [out]

The address of a caller-allocated variable that receives <b>true</b> if the component has been selected to be restored, or <b>false</b> otherwise.


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



<b>IsSelectedForRestore</b> is relevant only under component mode.

If the component defines a component set, 
<b>IsSelectedForRestore</b> refers both to the component and all of its subcomponents.




## -see-also




<a href="https://msdn.microsoft.com/8f8051d3-b1b6-418b-8a53-0ddc82a20bb3">IVssBackupComponents::SetSelectedForRestore</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>
 

 

