---
UID: NF:certenroll.ICspStatus.Initialize
title: ICspStatus::Initialize
author: windows-sdk-content
description: Initializes the object from a cryptographic provider and an associated algorithm.
old-location: security\icspstatus_initialize.htm
old-project: SecCertEnroll
ms.assetid: dc5f92e8-29fe-474c-bf1d-c6d7716abce1
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICspStatus interface [Security],Initialize method, ICspStatus.Initialize, ICspStatus::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICspStatus interface, certenroll/ICspStatus::Initialize, security.icspstatus_initialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspStatus::Initialize


## -description


The <b>Initialize</b> method initializes the object from a cryptographic provider and an associated algorithm. This method is web enabled.


## -parameters




### -param pCsp [in]

Pointer to an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> interface that represents information about the provider.


### -param pAlgorithm [in, optional]

Pointer to an  <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> interface that represents an algorithm supported by the provider identified in the  <i>pCsp</i> parameter. This parameter is optional and can be <b>NULL</b>.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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



The <b>Initialize</b> method saves the <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> and <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> objects you specify in the <a href="https://msdn.microsoft.com/9e9202ad-086e-493b-8830-0a0f8980cec5">CspInformation</a> and <a href="https://msdn.microsoft.com/fc86ff4a-98f4-4e14-8d24-132926c9b41d">CspAlgorithm</a> properties. The method also creates an empty <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object and saves it in the <a href="https://msdn.microsoft.com/56798477-ec12-47b6-a226-d20258677033">EnrollmentStatus</a> property.

An <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection is typically initialized by an <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object. The <b>Initialize</b> method has been provided so that you can create <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects to add to a custom collection.




## -see-also




<a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a>



<a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a>
 

 

