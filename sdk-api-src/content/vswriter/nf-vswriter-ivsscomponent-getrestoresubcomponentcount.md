---
UID: NF:vswriter.IVssComponent.GetRestoreSubcomponentCount
title: IVssComponent::GetRestoreSubcomponentCount
author: windows-sdk-content
description: The GetRestoreSubcomponentCount method returns the number of subcomponents associated with a component.
old-location: base\ivsscomponent_getrestoresubcomponentcount.htm
old-project: VSS
ms.assetid: 04c1dcdc-7672-4b7c-a9db-eafca80ab257
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetRestoreSubcomponentCount, GetRestoreSubcomponentCount method [VSS], GetRestoreSubcomponentCount method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetRestoreSubcomponentCount method, IVssComponent.GetRestoreSubcomponentCount, IVssComponent::GetRestoreSubcomponentCount, _win32_ivsscomponent_getrestoresubcomponentcount, base.ivsscomponent_getrestoresubcomponentcount, vswriter/IVssComponent::GetRestoreSubcomponentCount
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
 - IVssComponent.GetRestoreSubcomponentCount
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::GetRestoreSubcomponentCount


## -description


The 
<b>GetRestoreSubcomponentCount</b> method returns the number of subcomponents associated with a component.

Either a writer or a requester can call this method.


## -parameters




### -param pcRestoreSubcomponent [out]

The address of a caller-allocated variable that receives the number of subcomponents that are associated with a component.


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




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/23c37342-fcbd-4401-83d5-a52d4a69b908">IVssComponent::GetRestoreSubcomponent</a>
 

 

