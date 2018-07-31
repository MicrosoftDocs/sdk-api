---
UID: NF:vswriter.IVssComponent.GetComponentName
title: IVssComponent::GetComponentName
author: windows-sdk-content
description: The GetComponentName method returns the logical name of this component.
old-location: base\ivsscomponent_getcomponentname.htm
old-project: VSS
ms.assetid: 24b36ea6-3662-4846-a90b-5c2da578e1fa
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetComponentName, GetComponentName method [VSS], GetComponentName method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetComponentName method, IVssComponent.GetComponentName, IVssComponent::GetComponentName, _win32_ivsscomponent_getcomponentname, base.ivsscomponent_getcomponentname, vswriter/IVssComponent::GetComponentName
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
 - IVssComponent.GetComponentName
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::GetComponentName


## -description


The 
<b>GetComponentName</b> method returns the logical name of this component.

Either a writer or a requester can call this method.


## -parameters




### -param pbstrName






#### - pwszName [out]

Pointer to a string containing the logical name of the component.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This component has no name. This state should never occur.

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
 




## -remarks



The caller should free the memory held by the <i>pwszName</i> parameter by calling <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>
 

 

