---
UID: NF:certenroll.ICspStatus.Initialize
title: ICspStatus::Initialize
author: windows-sdk-content
description: Initializes the object from a cryptographic provider and an associated algorithm.
old-location: security\icspstatus_initialize.htm
tech.root: SecCertEnroll
ms.assetid: dc5f92e8-29fe-474c-bf1d-c6d7716abce1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICspStatus interface [Security],Initialize method, ICspStatus.Initialize, ICspStatus::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICspStatus interface, certenroll/ICspStatus::Initialize, security.icspstatus_initialize
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
 - ICspStatus.Initialize
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
- ICspStatus.Initialize
: 
---

# ICspStatus::Initialize


## -description


The <b>Initialize</b> method initializes the object from a cryptographic provider and an associated algorithm. This method is web enabled.


## -parameters




### -param pCsp [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> interface that represents information about the provider.


### -param pAlgorithm [in, optional]

Pointer to an  <a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a> interface that represents an algorithm supported by the provider identified in the  <i>pCsp</i> parameter. This parameter is optional and can be <b>NULL</b>.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
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



The <b>Initialize</b> method saves the <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a> objects you specify in the <a href="https://msdn.microsoft.com/en-us/library/Aa376773(v=VS.85).aspx">CspInformation</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa376772(v=VS.85).aspx">CspAlgorithm</a> properties. The method also creates an empty <a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a> object and saves it in the <a href="https://msdn.microsoft.com/en-us/library/Aa376775(v=VS.85).aspx">EnrollmentStatus</a> property.

An <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection is typically initialized by an <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object. The <b>Initialize</b> method has been provided so that you can create <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> objects to add to a custom collection.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a>
 

 

