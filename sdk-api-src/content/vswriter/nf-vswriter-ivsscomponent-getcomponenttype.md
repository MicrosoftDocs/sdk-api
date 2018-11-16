---
UID: NF:vswriter.IVssComponent.GetComponentType
title: IVssComponent::GetComponentType
author: windows-sdk-content
description: The GetComponentType method returns the type of this component in terms of the VSS_COMPONENT_TYPE enumeration.
old-location: base\ivsscomponent_getcomponenttype.htm
tech.root: VSS
ms.assetid: 89675df6-dcfd-4167-aa6f-5c88e619ef1c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetComponentType, GetComponentType method [VSS], GetComponentType method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetComponentType method, IVssComponent.GetComponentType, IVssComponent::GetComponentType, _win32_ivsscomponent_getcomponenttype, base.ivsscomponent_getcomponenttype, vswriter/IVssComponent::GetComponentType
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
 - IVssComponent.GetComponentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- IVssComponent.GetComponentType
: 
---

# IVssComponent::GetComponentType


## -description


The 
<b>GetComponentType</b> method returns the type of this component in terms of the 
<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a> enumeration.

Either a writer or a requester can call this method.


## -parameters




### -param pct [out]

The address of a caller-allocated variable that receives a 
<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a> enumeration value that specifies the type of the component.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>
 

 

