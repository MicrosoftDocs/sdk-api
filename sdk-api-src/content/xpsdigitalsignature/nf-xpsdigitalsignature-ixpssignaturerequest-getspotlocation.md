---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetSpotLocation
title: IXpsSignatureRequest::GetSpotLocation (xpsdigitalsignature.h)
description: Gets the page and the location on the page where the visible digital signature or the digital signature request will be displayed.
helpviewer_keywords: ["GetSpotLocation","GetSpotLocation method [XPS Documents and Packaging]","GetSpotLocation method [XPS Documents and Packaging]","IXpsSignatureRequest interface","IXpsSignatureRequest interface [XPS Documents and Packaging]","GetSpotLocation method","IXpsSignatureRequest.GetSpotLocation","IXpsSignatureRequest::GetSpotLocation","xps.ixpssignaturerequest_getspotlocation","xpsdigitalsignature/IXpsSignatureRequest::GetSpotLocation"]
old-location: xps\ixpssignaturerequest_getspotlocation.htm
tech.root: xps
ms.assetid: f8a93c77-c978-4483-b0e0-36d998add184
ms.date: 12/05/2018
ms.keywords: GetSpotLocation, GetSpotLocation method [XPS Documents and Packaging], GetSpotLocation method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetSpotLocation method, IXpsSignatureRequest.GetSpotLocation, IXpsSignatureRequest::GetSpotLocation, xps.ixpssignaturerequest_getspotlocation, xpsdigitalsignature/IXpsSignatureRequest::GetSpotLocation
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
 - IXpsSignatureRequest::GetSpotLocation
 - xpsdigitalsignature/IXpsSignatureRequest::GetSpotLocation
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
 - IXpsSignatureRequest.GetSpotLocation
---

# IXpsSignatureRequest::GetSpotLocation


## -description

Gets the page and the location on the page where the visible digital signature or the digital signature request will be displayed.

## -parameters

### -param pageIndex [out]

The index value of the FixedPage part that contains the signature or the digital signature request. If a spot location is not specified for the signature request, –1 is returned.

### -param pagePartName [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part that contains the FixedPage on which the digital signature is to be displayed.

### -param x [out]

The x-coordinate value of the signing spot on the page.

### -param y [out]

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pageIndex</i>, <i>pagePartName</i>, <i>x</i>, or <i>y</i>  is <b>NULL</b>.

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

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>