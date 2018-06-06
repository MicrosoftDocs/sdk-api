---
UID: NF:vswriter.IVssComponent.GetNewTargetCount
title: IVssComponent::GetNewTargetCount
author: windows-sdk-content
description: The GetNewTargetCount method returns the number of new target restore locations associated with a given component.
old-location: base\ivsscomponent_getnewtargetcount.htm
old-project: VSS
ms.assetid: b41afed9-2689-469e-b3c4-83cf18c5f8a9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetNewTargetCount, GetNewTargetCount method [VSS], GetNewTargetCount method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetNewTargetCount method, IVssComponent.GetNewTargetCount, IVssComponent::GetNewTargetCount, _win32_ivsscomponent_getnewtargetcount, base.ivsscomponent_getnewtargetcount, vswriter/IVssComponent::GetNewTargetCount
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
 - IVssComponent.GetNewTargetCount
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
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




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>
 

 

