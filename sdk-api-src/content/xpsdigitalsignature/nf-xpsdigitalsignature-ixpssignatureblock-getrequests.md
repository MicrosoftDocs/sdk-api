---
UID: NF:xpsdigitalsignature.IXpsSignatureBlock.GetRequests
title: IXpsSignatureBlock::GetRequests (xpsdigitalsignature.h)
description: Gets a pointer to the IXpsSignatureRequestCollection interface that contains a collection of signature requests.
helpviewer_keywords: ["GetRequests","GetRequests method [XPS Documents and Packaging]","GetRequests method [XPS Documents and Packaging]","IXpsSignatureBlock interface","IXpsSignatureBlock interface [XPS Documents and Packaging]","GetRequests method","IXpsSignatureBlock.GetRequests","IXpsSignatureBlock::GetRequests","xps.ixpssignatureblock_getrequests","xpsdigitalsignature/IXpsSignatureBlock::GetRequests"]
old-location: xps\ixpssignatureblock_getrequests.htm
tech.root: xps
ms.assetid: 97050917-8b41-4e4f-80c5-d8f166897c96
ms.date: 12/05/2018
ms.keywords: GetRequests, GetRequests method [XPS Documents and Packaging], GetRequests method [XPS Documents and Packaging],IXpsSignatureBlock interface, IXpsSignatureBlock interface [XPS Documents and Packaging],GetRequests method, IXpsSignatureBlock.GetRequests, IXpsSignatureBlock::GetRequests, xps.ixpssignatureblock_getrequests, xpsdigitalsignature/IXpsSignatureBlock::GetRequests
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
 - IXpsSignatureBlock::GetRequests
 - xpsdigitalsignature/IXpsSignatureBlock::GetRequests
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
 - IXpsSignatureBlock.GetRequests
---

# IXpsSignatureBlock::GetRequests


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection">IXpsSignatureRequestCollection</a> interface that contains a collection of signature requests.

## -parameters

### -param requests [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection">IXpsSignatureRequestCollection</a> interface that contains a collection of signature requests.

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
<i>requests</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
 The interface is not connected to the signature manager.

</td>
</tr>
</table>

## -remarks

Signature requests are added to the  collection of signature requests  by parsing the XML markup 
    of the corresponding SignatureDefinitions part while <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile">LoadPackageFile</a> or <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream">LoadPackageStream</a> reads the XPS package.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection">IXpsSignatureRequestCollection</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>