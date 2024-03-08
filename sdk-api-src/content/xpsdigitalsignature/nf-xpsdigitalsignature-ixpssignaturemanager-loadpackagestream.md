---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.LoadPackageStream
title: IXpsSignatureManager::LoadPackageStream (xpsdigitalsignature.h)
description: Loads an XPS package from a stream into the digital signature manager.
helpviewer_keywords: ["IXpsSignatureManager interface [XPS Documents and Packaging]","LoadPackageStream method","IXpsSignatureManager.LoadPackageStream","IXpsSignatureManager::LoadPackageStream","LoadPackageStream","LoadPackageStream method [XPS Documents and Packaging]","LoadPackageStream method [XPS Documents and Packaging]","IXpsSignatureManager interface","xps.ixpssignaturemanager_loadpackagestream","xpsdigitalsignature/IXpsSignatureManager::LoadPackageStream"]
old-location: xps\ixpssignaturemanager_loadpackagestream.htm
tech.root: xps
ms.assetid: 755bbd41-0941-4956-a99d-45b39f9b030f
ms.date: 12/05/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],LoadPackageStream method, IXpsSignatureManager.LoadPackageStream, IXpsSignatureManager::LoadPackageStream, LoadPackageStream, LoadPackageStream method [XPS Documents and Packaging], LoadPackageStream method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_loadpackagestream, xpsdigitalsignature/IXpsSignatureManager::LoadPackageStream
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
 - IXpsSignatureManager::LoadPackageStream
 - xpsdigitalsignature/IXpsSignatureManager::LoadPackageStream
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
 - IXpsSignatureManager.LoadPackageStream
---

# IXpsSignatureManager::LoadPackageStream


## -description

Loads an XPS package from a stream into the digital signature manager.

## -parameters

### -param stream [in]

The stream that contains the XPS package to be loaded.

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
<i>stream</i> is <b>NULL</b>.

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

 After the interface has been instantiated, the XPS package must be loaded by calling this method or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a> before
calling any other method  in this interface.

After an XPS package has been loaded into an instance of <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>, calling <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a> or <b>LoadPackageStream</b> in the same instance will return an error.

After <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a> or <b>LoadPackageStream</b> has been called, the same object cannot be reused for another XPS package file or stream. To load another XPS package, a new instance of the  <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a> must be instantiated.

<b>LoadPackageStream</b> does not validate all content of the XPS package; it does not, for example, detect invalid markup in a FixedPage part.

The implementation of the  <b>IStream</b> interface that is passed in <i>stream</i> must support random read access. The implementation must also contain only an XPS package and be positioned at the beginning of the stream before it can be used by this method.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>