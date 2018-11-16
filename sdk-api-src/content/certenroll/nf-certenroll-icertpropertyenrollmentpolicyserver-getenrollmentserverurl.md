---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerUrl
title: ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerUrl
author: windows-sdk-content
description: Retrieves a string that contains the URL for the certificate enrollment server.
old-location: security\icertpropertyenrollmentpolicyserver_getenrollmentserverurl.htm
tech.root: SecCertEnroll
ms.assetid: 6d8e7f45-f7ff-48d0-95d8-4d426e122554
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetEnrollmentServerUrl, GetEnrollmentServerUrl method [Security], GetEnrollmentServerUrl method [Security],ICertPropertyEnrollmentPolicyServer interface, ICertPropertyEnrollmentPolicyServer interface [Security],GetEnrollmentServerUrl method, ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerUrl, ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerUrl, certenroll/ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerUrl, security.icertpropertyenrollmentpolicyserver_getenrollmentserverurl
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerUrl
: 
---

# ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerUrl


## -description


The <b>GetEnrollmentServerUrl</b> method retrieves a string that contains the URL for the certificate enrollment server. This value is set by the <a href="https://msdn.microsoft.com/en-us/library/Ee351591(v=VS.85).aspx">Initialize</a> method.


## -parameters




### -param pValue [out, retval]

Pointer to a <b>BSTR</b> that receives the URL.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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




<a href="https://msdn.microsoft.com/en-us/library/Ee338624(v=VS.85).aspx">ICertPropertyEnrollmentPolicyServer</a>
 

 

