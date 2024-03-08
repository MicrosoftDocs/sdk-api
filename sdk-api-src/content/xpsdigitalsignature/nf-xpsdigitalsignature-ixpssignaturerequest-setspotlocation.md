---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.SetSpotLocation
title: IXpsSignatureRequest::SetSpotLocation (xpsdigitalsignature.h)
description: Specifies the page and the location on the page where the visible digital signature or the digital signature request will be displayed.
helpviewer_keywords: ["IXpsSignatureRequest interface [XPS Documents and Packaging]","SetSpotLocation method","IXpsSignatureRequest.SetSpotLocation","IXpsSignatureRequest::SetSpotLocation","SetSpotLocation","SetSpotLocation method [XPS Documents and Packaging]","SetSpotLocation method [XPS Documents and Packaging]","IXpsSignatureRequest interface","xps.ixpssignaturerequest_setspotlocation","xpsdigitalsignature/IXpsSignatureRequest::SetSpotLocation"]
old-location: xps\ixpssignaturerequest_setspotlocation.htm
tech.root: xps
ms.assetid: 44ee13dd-ceea-4cd3-8c9e-4300c0c304ab
ms.date: 12/05/2018
ms.keywords: IXpsSignatureRequest interface [XPS Documents and Packaging],SetSpotLocation method, IXpsSignatureRequest.SetSpotLocation, IXpsSignatureRequest::SetSpotLocation, SetSpotLocation, SetSpotLocation method [XPS Documents and Packaging], SetSpotLocation method [XPS Documents and Packaging],IXpsSignatureRequest interface, xps.ixpssignaturerequest_setspotlocation, xpsdigitalsignature/IXpsSignatureRequest::SetSpotLocation
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
 - IXpsSignatureRequest::SetSpotLocation
 - xpsdigitalsignature/IXpsSignatureRequest::SetSpotLocation
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
 - IXpsSignatureRequest.SetSpotLocation
---

# IXpsSignatureRequest::SetSpotLocation


## -description

Specifies the page and the  location on the page  where   the visible digital signature or the digital signature request  will be displayed.

## -parameters

### -param pageIndex [in]

The index value of the FixedPage part in the XPS document  that contains the visible digital signature or the digital signature request.

If the value of this parameter is –1, a <b>SpotLocation</b> element will not be written to the SignatureDefinitions markup.

If the value of this parameter is not –1, it must be a page number that exists in the FixedDocument part to which the signature block that contains this request is attached.

### -param x [in]

The x-coordinate value of the signing spot on the page.

### -param y [in]

The y-coordinate value of the signing spot on the page.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
 The interface is not connected to the signature manager.

</td>
</tr>
</table>

## -remarks

The location  of the signing spot is specified in XPS units from the upper-left corner of the page. There are 96 XPS units per inch.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>