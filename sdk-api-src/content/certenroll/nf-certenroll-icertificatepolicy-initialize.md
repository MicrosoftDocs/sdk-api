---
UID: NF:certenroll.ICertificatePolicy.Initialize
title: ICertificatePolicy::Initialize
author: windows-sdk-content
description: Initializes the object from an object identifier (OID).
old-location: security\icertificatepolicy_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 995b344b-ed1f-47e4-a7c6-0d638ed9ec23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertificatePolicy interface [Security],Initialize method, ICertificatePolicy.Initialize, ICertificatePolicy::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertificatePolicy interface, certenroll/ICertificatePolicy::Initialize, security.icertificatepolicy_initialize_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertificatePolicy.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificatePolicy::Initialize


## -description


The <b>Initialize</b> method initializes the object from an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface that represents the OID.


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
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



You must use an initialized <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> object when calling this method. All of the  <b>IObjectId</b> initialization methods search  the registry and static memory on the local computer and Active Directory on the domain server for the first OID that matches the specified initialization parameters. You can retrieve the OID by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375228(v=VS.85).aspx">ObjectId</a> property.

When you call the <b>Initialize</b> method, an empty <a href="https://msdn.microsoft.com/en-us/library/Aa376804(v=VS.85).aspx">IPolicyQualifiers</a> object is created. You can retrieve the object by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375229(v=VS.85).aspx">PolicyQualifiers</a> property. You can use the object to define policy qualifiers if you are creating a <b>CertificatePolicies</b> extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375214(v=VS.85).aspx">ICertificatePolicies</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375225(v=VS.85).aspx">ICertificatePolicy</a>
 

 

