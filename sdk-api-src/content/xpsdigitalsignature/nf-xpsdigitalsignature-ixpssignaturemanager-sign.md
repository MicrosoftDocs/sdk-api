---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.Sign
title: IXpsSignatureManager::Sign
author: windows-sdk-content
description: Signs the contents of an XPS package as specified by the signing options and returns the resulting digital signature.
old-location: xps\ixpssignaturemanager_sign.htm
tech.root: printdocs
ms.assetid: 82a57ca8-edc7-4248-92d1-8092f6dce4f8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],Sign method, IXpsSignatureManager.Sign, IXpsSignatureManager::Sign, Sign, Sign method [XPS Documents and Packaging], Sign method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_sign, xpsdigitalsignature/IXpsSignatureManager::Sign
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.Sign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureManager::Sign


## -description


Signs the contents of an  XPS package as specified by the signing options and returns the resulting digital signature.


## -parameters




### -param signOptions [in]

A pointer to the <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface that contains the  signing options.

<div class="alert"><b>Note</b>  <p class="note">The SignatureMethod and the DigestMethod properties of the <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface must be initialized before the pointer to that interface can be used in the <i>signOptions</i> parameter.

</div>
<div> </div>

### -param x509Certificate [in]

A pointer to the <a href="_crypto2_cert_context">CERT_CONTEXT</a> structure that contains the X.509 certificate to be used for signing.


### -param signature [out, retval]

A pointer to the  <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface that contains the new digital signature.

If successful, this method creates the signature part, adds it to the package, and in <i>signature</i> returns a pointer to the interface of that signature part.


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
<dt><b>XPS_E_MARKUP_COMPATIBILITY_ELEMENTS</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/36fa92d4-ffd4-4666-8d3e-02436e3bb464">XPS_SIGN_FLAGS</a> value specified that no markup compatibility elements were expected; however, markup compatibility elements were  found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>signOptions</i> does not point to a recognized interface implementation.  Custom implementation of XPS Document API interfaces is not supported.

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



Adding a new signature does not overwrite the original file or stream that was read by calling the <a href="https://msdn.microsoft.com/ecb33eee-4622-4a2e-bc24-7a77d16ef4a4">LoadPackageFile</a> or <a href="https://msdn.microsoft.com/755bbd41-0941-4956-a99d-45b39f9b030f">LoadPackageStream</a> method. 
    The signature will be added to the in-memory copy of the XPS package until the package is  saved (by calling the <a href="https://msdn.microsoft.com/954d8eb1-8680-410b-909b-da7a6572c0f3">SavePackageToFile</a> or <a href="https://msdn.microsoft.com/1a29c8e2-2e5d-4cc0-adfd-6debabca9243">SavePackageToStream</a> method).

If the new signature includes parts that contain markup compatibility elements, the default is for this method to fail with an error  of <b>XPS_E_MARKUP_COMPATIBILITY_ELEMENTS</b>. 
     To override this behavior, call <a href="https://msdn.microsoft.com/59467fd5-c462-4827-a4f8-e152df981ace">IXpsSigningOptions::SetFlags</a>; this will set the <b>XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY</b> flag in the <a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a> interface referenced by the <i>signOptions</i> parameter.

If this method returns an <b>HRESULT</b> value that is not in the list of its return values, the signature manager should be released and recreated.

This method will succeed  even if the new signature breaks existing signatures.




## -see-also




<a href="_crypto2_cert_context">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

