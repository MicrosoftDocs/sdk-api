---
UID: NF:certenroll.IX509EnrollmentPolicyServer.InitializeImport
title: IX509EnrollmentPolicyServer::InitializeImport
author: windows-driver-content
description: Initializes the certificate enrollment policy (CEP) server from a collection of templates and object identifiers.
old-location: security\ix509enrollmentpolicyserver_initializeimport.htm
old-project: SecCertEnroll
ms.assetid: b397f57f-e01e-4c2b-8338-892f56b76c9e
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509EnrollmentPolicyServer interface [Security],InitializeImport method, IX509EnrollmentPolicyServer.InitializeImport, IX509EnrollmentPolicyServer::InitializeImport, InitializeImport, InitializeImport method [Security], InitializeImport method [Security],IX509EnrollmentPolicyServer interface, certenroll/IX509EnrollmentPolicyServer::InitializeImport, security.ix509enrollmentpolicyserver_initializeimport
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenroll.h
api_name:
-	IX509EnrollmentPolicyServer.InitializeImport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509EnrollmentPolicyServer::InitializeImport


## -description


The <b>InitializeImport</b> method initializes the certificate enrollment policy (CEP) server from a collection of templates and object identifiers.


## -parameters




### -param val [in]

A <b>VARIANT</b> of type <b>VT_ARRAY|VT_UI1</b> that contains the templates and object identifiers.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The  <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> object has already been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)</b></dt>
</dl>
</td>
<td width="60%">
The <b>VARIANT</b> in the <i>val</i> parameter is not of type <b>VT_ARRAY</b>.

</td>
</tr>
</table>
 




## -remarks



Call this method to import templates and OIDs previously written to a buffer by the <a href="https://msdn.microsoft.com/b821329b-2ec6-4f47-ba5f-2e1cd7ffb06f">Export</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

