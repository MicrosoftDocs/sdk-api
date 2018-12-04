---
UID: NF:vswriter.IVssComponent.GetNewTarget
title: IVssComponent::GetNewTarget
author: windows-sdk-content
description: The GetNewTarget method returns the new file restoration locations for the selected component or component set.
old-location: base\ivsscomponent_getnewtarget.htm
tech.root: vss
ms.assetid: 21f22fae-2230-418b-8942-754c863a9213
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetNewTarget, GetNewTarget method [VSS], GetNewTarget method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetNewTarget method, IVssComponent.GetNewTarget, IVssComponent::GetNewTarget, _win32_ivsscomponent_getnewtarget, base.ivsscomponent_getnewtarget, vswriter/IVssComponent::GetNewTarget
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVssComponent.GetNewTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssComponent::GetNewTarget


## -description


The 
<b>GetNewTarget</b> method returns the new file restoration locations for the selected component or component set. (See 
<a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability and Logical Paths</a> for information on selecting components.)

Either a writer or a requester can call this method.


## -parameters




### -param iNewTarget [in]

Index number of the new target. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of new targets associated with a given component. The value of <i>n</i> is returned by 
<a href="https://msdn.microsoft.com/b41afed9-2689-469e-b3c4-83cf18c5f8a9">IVssComponent::GetNewTargetCount</a>.


### -param ppFiledesc [out]

Doubly indirect pointer to an 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object containing the new target restore location information.


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
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

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



New targets returned by 
<b>GetNewTarget</b> may be those not only of files in the current component but to files in any of its nonselectable subcomponents.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/b41afed9-2689-469e-b3c4-83cf18c5f8a9">IVssComponent::GetNewTargetCount</a>
 

 

