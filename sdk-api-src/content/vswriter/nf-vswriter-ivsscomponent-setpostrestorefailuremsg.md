---
UID: NF:vswriter.IVssComponent.SetPostRestoreFailureMsg
title: IVssComponent::SetPostRestoreFailureMsg
author: windows-sdk-content
description: The SetPostRestoreFailureMsg method is used to create a message describing a failure in processing a PostRestore event.
old-location: base\ivsscomponent_setpostrestorefailuremsg.htm
old-project: VSS
ms.assetid: 1059a586-69e2-4a02-8f52-b8da3f04f51c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssComponent interface [VSS],SetPostRestoreFailureMsg method, IVssComponent.SetPostRestoreFailureMsg, IVssComponent::SetPostRestoreFailureMsg, SetPostRestoreFailureMsg, SetPostRestoreFailureMsg method [VSS], SetPostRestoreFailureMsg method [VSS],IVssComponent interface, _win32_ivsscomponent_setpostrestorefailuremsg, base.ivsscomponent_setpostrestorefailuremsg, vswriter/IVssComponent::SetPostRestoreFailureMsg
ms.prod: windows
ms.technology: windows-sdk
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
 - IVssComponent.SetPostRestoreFailureMsg
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::SetPostRestoreFailureMsg


## -description


The 
<b>SetPostRestoreFailureMsg</b> method is used to create a message describing a failure in processing a 
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event.

Only a writer can call this method, and only during a restore operation.


## -parameters




### -param wszPostRestoreFailureMsg [in]

A caller-allocated <b>NULL</b>-terminated wide character string containing the failure message that describes an error that occurred while processing a 
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event.


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
Successfully set the failure message.

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



The failure message set by 
<b>SetPostRestoreFailureMsg</b> applies to all files in the component and any nonselectable subcomponents.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/f7d236e9-bd83-4685-b249-4e5b8ada535a">IVssComponent::GetPostRestoreFailureMsg</a>



<a href="https://msdn.microsoft.com/58c007a8-8414-4e2d-8042-d249a723780a">IVssComponent::GetPreRestoreFailureMsg</a>



<a href="https://msdn.microsoft.com/5b273cba-9878-4494-81ef-af1367f1e0a5">IVssComponent::SetPreRestoreFailureMsg</a>
 

 

