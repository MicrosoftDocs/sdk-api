---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.CreateSigningOptions
title: IXpsSignatureManager::CreateSigningOptions
author: windows-sdk-content
description: Creates a new IXpsSigningOptions interface.
old-location: xps\ixpssignaturemanager_createsigningoptions.htm
old-project: printdocs
ms.assetid: 0f64f46a-905a-48cf-9e7a-f6cc1b2d6450
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateSigningOptions, CreateSigningOptions method [XPS Documents and Packaging], CreateSigningOptions method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],CreateSigningOptions method, IXpsSignatureManager.CreateSigningOptions, IXpsSignatureManager::CreateSigningOptions, xps.ixpssignaturemanager_createsigningoptions, xpsdigitalsignature/IXpsSignatureManager::CreateSigningOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_SIGN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.CreateSigningOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureManager::CreateSigningOptions


## -description


Creates a new  <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface.


## -parameters




### -param signingOptions [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a> and  <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>signingOptions</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has not yet been opened in the signature manager.

</td>
</tr>
</table>
 




## -remarks



The new  <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface can be used to set the signing options for the <a href="https://msdn.microsoft.com/82a57ca8-edc7-4248-92d1-8092f6dce4f8">Sign</a> method; however, the SignatureMethod and the DigestMethod  properties must be initialized before the new interface  can be used as a parameter of the <b>Sign</b> method.

The <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface created by this method can be used in more than one call to the <a href="https://msdn.microsoft.com/82a57ca8-edc7-4248-92d1-8092f6dce4f8">Sign</a> method.




## -see-also




<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

