---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.SetSpotLocation
title: IXpsSignatureRequest::SetSpotLocation
author: windows-sdk-content
description: Specifies the page and the location on the page where the visible digital signature or the digital signature request will be displayed.
old-location: xps\ixpssignaturerequest_setspotlocation.htm
tech.root: printdocs
ms.assetid: 44ee13dd-ceea-4cd3-8c9e-4300c0c304ab
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IXpsSignatureRequest interface [XPS Documents and Packaging],SetSpotLocation method, IXpsSignatureRequest.SetSpotLocation, IXpsSignatureRequest::SetSpotLocation, SetSpotLocation, SetSpotLocation method [XPS Documents and Packaging], SetSpotLocation method [XPS Documents and Packaging],IXpsSignatureRequest interface, xps.ixpssignaturerequest_setspotlocation, xpsdigitalsignature/IXpsSignatureRequest::SetSpotLocation
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
 - IXpsSignatureRequest.SetSpotLocation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

