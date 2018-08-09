---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.GetPolicyServerUrl
title: ICertPropertyEnrollmentPolicyServer::GetPolicyServerUrl
author: windows-sdk-content
description: Retrieves a string that contains the URL for the certificate enrollment policy (CEP) server.
old-location: security\icertpropertyenrollmentpolicyserver_getpolicyserverurl.htm
old-project: seccertenroll
ms.assetid: 9d7ba049-4566-423d-b750-ff091dce1e2a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPolicyServerUrl, GetPolicyServerUrl method [Security], GetPolicyServerUrl method [Security],ICertPropertyEnrollmentPolicyServer interface, ICertPropertyEnrollmentPolicyServer interface [Security],GetPolicyServerUrl method, ICertPropertyEnrollmentPolicyServer.GetPolicyServerUrl, ICertPropertyEnrollmentPolicyServer::GetPolicyServerUrl, certenroll/ICertPropertyEnrollmentPolicyServer::GetPolicyServerUrl, security.icertpropertyenrollmentpolicyserver_getpolicyserverurl
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
 - ICertPropertyEnrollmentPolicyServer.GetPolicyServerUrl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICertPropertyEnrollmentPolicyServer::GetPolicyServerUrl


## -description


The <b>GetPolicyServerUrl</b> method retrieves a string that contains the URL for the certificate enrollment policy (CEP) server. This value is set by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method.


## -parameters




### -param pValue [out, retval]

Pointer to a <b>BSTR</b> that receives the URL.


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
 




## -see-also




<a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a>
 

 

