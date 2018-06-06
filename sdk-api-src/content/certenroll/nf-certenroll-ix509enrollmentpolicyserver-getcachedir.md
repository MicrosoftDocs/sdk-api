---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetCacheDir
title: IX509EnrollmentPolicyServer::GetCacheDir
author: windows-sdk-content
description: Retrieves the name of the directory on the certificate enrollment policy (CEP) server that contains the policy cache file.
old-location: security\ix509enrollmentpolicyserver_getcachedir.htm
old-project: SecCertEnroll
ms.assetid: 72b0b6f0-cc4f-4e03-9b6c-7bd4c12cf0a3
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetCacheDir, GetCacheDir method [Security], GetCacheDir method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetCacheDir method, IX509EnrollmentPolicyServer.GetCacheDir, IX509EnrollmentPolicyServer::GetCacheDir, certenroll/IX509EnrollmentPolicyServer::GetCacheDir, security.ix509enrollmentpolicyserver_getcachedir
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
 - IX509EnrollmentPolicyServer.GetCacheDir
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509EnrollmentPolicyServer::GetCacheDir


## -description


The <b>GetCacheDir</b> method retrieves the name of the directory on the certificate enrollment policy (CEP) server that contains the policy cache file.


## -parameters




### -param pValue [out, retval]

Pointer to a <b>BSTR</b> that receives the directory name.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The cache directory could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter must not be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> has not been initialized.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

