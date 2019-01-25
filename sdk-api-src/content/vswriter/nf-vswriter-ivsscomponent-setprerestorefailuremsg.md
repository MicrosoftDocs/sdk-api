---
UID: NF:vswriter.IVssComponent.SetPreRestoreFailureMsg
title: IVssComponent::SetPreRestoreFailureMsg
author: windows-sdk-content
description: The SetPreRestoreFailureMsg method is used to create a message describing a failure in processing a PreRestore event.
old-location: base\ivsscomponent_setprerestorefailuremsg.htm
tech.root: VSS
ms.assetid: 5b273cba-9878-4494-81ef-af1367f1e0a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssComponent interface [VSS],SetPreRestoreFailureMsg method, IVssComponent.SetPreRestoreFailureMsg, IVssComponent::SetPreRestoreFailureMsg, SetPreRestoreFailureMsg, SetPreRestoreFailureMsg method [VSS], SetPreRestoreFailureMsg method [VSS],IVssComponent interface, _win32_ivsscomponent_setprerestorefailuremsg, base.ivsscomponent_setprerestorefailuremsg, vswriter/IVssComponent::SetPreRestoreFailureMsg
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponent.SetPreRestoreFailureMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssComponent::SetPreRestoreFailureMsg


## -description


The <b>SetPreRestoreFailureMsg</b> 
    method is used to create a message describing a failure in processing a 
    <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event.

Only a writer can call this method, and only during a restore operation.


## -parameters




### -param wszPreRestoreFailureMsg [in]

A caller-allocated <b>NULL</b>-terminated wide character string containing the failure message describing an error that occurred 
      while processing a <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> 
      event.


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
    <b>SetPreRestoreFailureMsg</b> applies to 
    all files in the component and any nonselectable subcomponents.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/f7d236e9-bd83-4685-b249-4e5b8ada535a">IVssComponent::GetPostRestoreFailureMsg</a>



<a href="https://msdn.microsoft.com/58c007a8-8414-4e2d-8042-d249a723780a">IVssComponent::GetPreRestoreFailureMsg</a>



<a href="https://msdn.microsoft.com/1059a586-69e2-4a02-8f52-b8da3f04f51c">IVssComponent::SetPostRestoreFailureMsg</a>
 

 

