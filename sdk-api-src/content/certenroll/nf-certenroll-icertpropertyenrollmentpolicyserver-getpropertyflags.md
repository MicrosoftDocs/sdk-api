---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICertPropertyEnrollmentPolicyServer::GetPropertyFlags


## -description


The <b>GetPropertyFlags</b> method retrieves a value that specifies the default policy server URL. This value is set by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method.


## -parameters




### -param pValue [out, retval]

Pointer to an <a href="https://msdn.microsoft.com/531502ac-8e89-46ee-a426-86e22a9dbe8d">EnrollmentPolicyServerPropertyFlags</a> enumeration value that contains the flag. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DefaultNone"></a><a id="defaultnone"></a><a id="DEFAULTNONE"></a><dl>
<dt><b>DefaultNone</b></dt>
</dl>
</td>
<td width="60%">
No default policy server URL has been specified.

</td>
</tr>
<tr>
<td width="40%"><a id="DefaultPolicyServer"></a><a id="defaultpolicyserver"></a><a id="DEFAULTPOLICYSERVER"></a><dl>
<dt><b>DefaultPolicyServer</b></dt>
</dl>
</td>
<td width="60%">
The policy server URL returned by <a href="https://msdn.microsoft.com/9d7ba049-4566-423d-b750-ff091dce1e2a">GetPolicyServerUrl</a> is the default value when an URL has not been specified.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a>
 

 

