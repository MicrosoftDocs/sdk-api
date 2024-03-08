---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.Sign
title: IXpsSignatureManager::Sign (xpsdigitalsignature.h)
description: Signs the contents of an XPS package as specified by the signing options and returns the resulting digital signature.
helpviewer_keywords: ["IXpsSignatureManager interface [XPS Documents and Packaging]","Sign method","IXpsSignatureManager.Sign","IXpsSignatureManager::Sign","Sign","Sign method [XPS Documents and Packaging]","Sign method [XPS Documents and Packaging]","IXpsSignatureManager interface","xps.ixpssignaturemanager_sign","xpsdigitalsignature/IXpsSignatureManager::Sign"]
old-location: xps\ixpssignaturemanager_sign.htm
tech.root: xps
ms.assetid: 82a57ca8-edc7-4248-92d1-8092f6dce4f8
ms.date: 12/05/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],Sign method, IXpsSignatureManager.Sign, IXpsSignatureManager::Sign, Sign, Sign method [XPS Documents and Packaging], Sign method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_sign, xpsdigitalsignature/IXpsSignatureManager::Sign
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsSignatureManager::Sign
 - xpsdigitalsignature/IXpsSignatureManager::Sign
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.Sign
---

# IXpsSignatureManager::Sign


## -description

Signs the contents of an  XPS package as specified by the signing options and returns the resulting digital signature.

## -parameters

### -param signOptions [in]

A pointer to the <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface that contains the  signing options.

<div class="alert"><b>Note</b>  <p class="note">The SignatureMethod and the DigestMethod properties of the <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface must be initialized before the pointer to that interface can be used in the <i>signOptions</i> parameter.

</div>
<div> </div>

### -param x509Certificate [in]

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the X.509 certificate to be used for signing.

### -param signature [out, retval]

A pointer to the  <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a> interface that contains the new digital signature.

If successful, this method creates the signature part, adds it to the package, and in <i>signature</i> returns a pointer to the interface of that signature part.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a> and  <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
The <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">XPS_SIGN_FLAGS</a> value specified that no markup compatibility elements were expected; however, markup compatibility elements were  found.

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

Adding a new signature does not overwrite the original file or stream that was read by calling the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a> or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a> method. 
    The signature will be added to the in-memory copy of the XPS package until the package is  saved (by calling the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-savepackagetofile">SavePackageToFile</a> or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-savepackagetostream">SavePackageToStream</a> method).

If the new signature includes parts that contain markup compatibility elements, the default is for this method to fail with an error  of <b>XPS_E_MARKUP_COMPATIBILITY_ELEMENTS</b>. 
     To override this behavior, call <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags">IXpsSigningOptions::SetFlags</a>; this will set the <b>XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY</b> flag in the <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface referenced by the <i>signOptions</i> parameter.

If this method returns an <b>HRESULT</b> value that is not in the list of its return values, the signature manager should be released and recreated.

This method will succeed  even if the new signature breaks existing signatures.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>