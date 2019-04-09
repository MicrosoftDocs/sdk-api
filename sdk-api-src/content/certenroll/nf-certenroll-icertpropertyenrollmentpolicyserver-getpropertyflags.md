---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.GetPropertyFlags
title: ICertPropertyEnrollmentPolicyServer::GetPropertyFlags (certenroll.h)
author: windows-sdk-content
description: Retrieves a value that specifies the default policy server URL.
old-location: security\icertpropertyenrollmentpolicyserver_getpropertyflags.htm
tech.root: seccertenroll
ms.assetid: 80d1af3c-2d1a-4d19-aed6-8cb2d3e52535
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DefaultNone, DefaultPolicyServer, GetPropertyFlags, GetPropertyFlags method [Security], GetPropertyFlags method [Security],ICertPropertyEnrollmentPolicyServer interface, ICertPropertyEnrollmentPolicyServer interface [Security],GetPropertyFlags method, ICertPropertyEnrollmentPolicyServer.GetPropertyFlags, ICertPropertyEnrollmentPolicyServer::GetPropertyFlags, certenroll/ICertPropertyEnrollmentPolicyServer::GetPropertyFlags, security.icertpropertyenrollmentpolicyserver_getpropertyflags
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - ICertPropertyEnrollmentPolicyServer.GetPropertyFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyEnrollmentPolicyServer::GetPropertyFlags


## -description


The <b>GetPropertyFlags</b> method retrieves a value that specifies the default policy server URL. This value is set by the <a href="https://msdn.microsoft.com/5d54ffb2-4a81-4d52-80db-b8526a52bb53">Initialize</a> method.


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
 

 

