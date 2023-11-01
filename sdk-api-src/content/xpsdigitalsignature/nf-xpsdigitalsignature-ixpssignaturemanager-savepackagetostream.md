---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.SavePackageToStream
title: IXpsSignatureManager::SavePackageToStream (xpsdigitalsignature.h)
description: Saves the XPS package by writing it to a stream.
helpviewer_keywords: ["IXpsSignatureManager interface [XPS Documents and Packaging]","SavePackageToStream method","IXpsSignatureManager.SavePackageToStream","IXpsSignatureManager::SavePackageToStream","SavePackageToStream","SavePackageToStream method [XPS Documents and Packaging]","SavePackageToStream method [XPS Documents and Packaging]","IXpsSignatureManager interface","xps.ixpssignaturemanager_savepackagetostream","xpsdigitalsignature/IXpsSignatureManager::SavePackageToStream"]
old-location: xps\ixpssignaturemanager_savepackagetostream.htm
tech.root: xps
ms.assetid: 1a29c8e2-2e5d-4cc0-adfd-6debabca9243
ms.date: 12/05/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],SavePackageToStream method, IXpsSignatureManager.SavePackageToStream, IXpsSignatureManager::SavePackageToStream, SavePackageToStream, SavePackageToStream method [XPS Documents and Packaging], SavePackageToStream method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_savepackagetostream, xpsdigitalsignature/IXpsSignatureManager::SavePackageToStream
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
 - IXpsSignatureManager::SavePackageToStream
 - xpsdigitalsignature/IXpsSignatureManager::SavePackageToStream
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
 - IXpsSignatureManager.SavePackageToStream
---

# IXpsSignatureManager::SavePackageToStream


## -description

Saves the XPS package by writing it to a stream.

## -parameters

### -param stream [in]

The stream to which the XPS package is written.

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
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has not yet been opened in the signature manager.

</td>
</tr>
</table>

## -remarks

If this method returns an <b>HRESULT</b> value that is not in the list of return values for this method, the signature manager should be released and recreated.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>