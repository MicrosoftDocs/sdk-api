---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.GetRequestIdString
title: ICertPropertyEnrollmentPolicyServer::GetRequestIdString
author: windows-sdk-content
description: Retrieves a unique string identifier for the certificate request sent to the certification authority during enrollment.
old-location: security\icertpropertyenrollmentpolicyserver_getrequestidstring.htm
old-project: seccertenroll
ms.assetid: c9855a9d-938f-4579-8447-a931dbba1428
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetRequestIdString, GetRequestIdString method [Security], GetRequestIdString method [Security],ICertPropertyEnrollmentPolicyServer interface, ICertPropertyEnrollmentPolicyServer interface [Security],GetRequestIdString method, ICertPropertyEnrollmentPolicyServer.GetRequestIdString, ICertPropertyEnrollmentPolicyServer::GetRequestIdString, certenroll/ICertPropertyEnrollmentPolicyServer::GetRequestIdString, security.icertpropertyenrollmentpolicyserver_getrequestidstring
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - ICertPropertyEnrollmentPolicyServer.GetRequestIdString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICertPropertyEnrollmentPolicyServer::GetRequestIdString


## -description


The <b>GetRequestIdString</b> method retrieves a unique string identifier for the certificate request sent to the certification authority during enrollment.


## -parameters




### -param pValue [out, retval]

Pointer to a <b>BSTR</b> that receives the ID string.


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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The property value is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available to create the URL string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(OLE_E_BLANK)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The property value has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The string can contain any information that uniquely identifies the certificate request.  This value is set when you call  the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a>
 

 

