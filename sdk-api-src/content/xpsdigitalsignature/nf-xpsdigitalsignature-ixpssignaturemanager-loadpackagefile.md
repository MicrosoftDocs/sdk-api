---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.LoadPackageFile
title: IXpsSignatureManager::LoadPackageFile (xpsdigitalsignature.h)
description: Loads an existing XPS package from a file into the digital signature manager.
helpviewer_keywords: ["IXpsSignatureManager interface [XPS Documents and Packaging]","LoadPackageFile method","IXpsSignatureManager.LoadPackageFile","IXpsSignatureManager::LoadPackageFile","LoadPackageFile","LoadPackageFile method [XPS Documents and Packaging]","LoadPackageFile method [XPS Documents and Packaging]","IXpsSignatureManager interface","xps.ixpssignaturemanager_loadpackagefile","xpsdigitalsignature/IXpsSignatureManager::LoadPackageFile"]
old-location: xps\ixpssignaturemanager_loadpackagefile.htm
tech.root: xps
ms.assetid: ecb33eee-4622-4a2e-bc24-7a77d16ef4a4
ms.date: 12/05/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],LoadPackageFile method, IXpsSignatureManager.LoadPackageFile, IXpsSignatureManager::LoadPackageFile, LoadPackageFile, LoadPackageFile method [XPS Documents and Packaging], LoadPackageFile method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_loadpackagefile, xpsdigitalsignature/IXpsSignatureManager::LoadPackageFile
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
 - IXpsSignatureManager::LoadPackageFile
 - xpsdigitalsignature/IXpsSignatureManager::LoadPackageFile
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
 - IXpsSignatureManager.LoadPackageFile
---

# IXpsSignatureManager::LoadPackageFile


## -description

Loads an existing XPS package from a file into the digital signature manager.

## -parameters

### -param fileName [in]

The file name of the XPS package to be loaded.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>fileName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_PACKAGE_ALREADY_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has already  been opened in the signature manager.

</td>
</tr>
</table>

## -remarks

 After the interface has been instantiated, the XPS package must be loaded by calling this method or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a> before
calling any other method in this interface.

After an XPS package has been loaded into an instance of <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>, calling <b>LoadPackageFile</b> or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a> in the same instance will return an error.

After <b>LoadPackageFile</b> or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a> has been called, the same object cannot be reused for another XPS package file or stream. To load another XPS package, a new instance of   <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a> must be instantiated.


<a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a> does not validate all content of the XPS package; it does not, for example, detect invalid markup in a FixedPage part.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>