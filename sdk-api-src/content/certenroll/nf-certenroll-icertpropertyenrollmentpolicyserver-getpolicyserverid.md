---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.GetPolicyServerId
title: ICertPropertyEnrollmentPolicyServer::GetPolicyServerId (certenroll.h)
description: Retrieves a string that uniquely identifies the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetPolicyServerId","GetPolicyServerId method [Security]","GetPolicyServerId method [Security]","ICertPropertyEnrollmentPolicyServer interface","ICertPropertyEnrollmentPolicyServer interface [Security]","GetPolicyServerId method","ICertPropertyEnrollmentPolicyServer.GetPolicyServerId","ICertPropertyEnrollmentPolicyServer::GetPolicyServerId","certenroll/ICertPropertyEnrollmentPolicyServer::GetPolicyServerId","security.icertpropertyenrollmentpolicyserver_getpolicyserverid"]
old-location: security\icertpropertyenrollmentpolicyserver_getpolicyserverid.htm
tech.root: security
ms.assetid: e0cd9f41-d697-4c27-9aff-a37de62d1bad
ms.date: 12/05/2018
ms.keywords: GetPolicyServerId, GetPolicyServerId method [Security], GetPolicyServerId method [Security],ICertPropertyEnrollmentPolicyServer interface, ICertPropertyEnrollmentPolicyServer interface [Security],GetPolicyServerId method, ICertPropertyEnrollmentPolicyServer.GetPolicyServerId, ICertPropertyEnrollmentPolicyServer::GetPolicyServerId, certenroll/ICertPropertyEnrollmentPolicyServer::GetPolicyServerId, security.icertpropertyenrollmentpolicyserver_getpolicyserverid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertPropertyEnrollmentPolicyServer::GetPolicyServerId
 - certenroll/ICertPropertyEnrollmentPolicyServer::GetPolicyServerId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - ICertPropertyEnrollmentPolicyServer.GetPolicyServerId
---

# ICertPropertyEnrollmentPolicyServer::GetPolicyServerId


## -description

The <b>GetPolicyServerId</b> method retrieves a string that uniquely identifies the certificate enrollment policy (CEP) server. This value is set by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a> method.

## -parameters

### -param pValue [out, retval]

Pointer to a <b>BSTR</b> that receives the ID string.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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
<dt><b>HRESULT_FROM_WIN32(OLE_E_BLANK)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The property value has not been initialized.

</td>
</tr>
</table>

## -remarks

The ID can be any string. It is set by the administrator who installs the CEP server.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a>