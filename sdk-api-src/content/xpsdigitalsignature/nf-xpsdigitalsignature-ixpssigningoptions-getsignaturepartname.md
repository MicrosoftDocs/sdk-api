---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetSignaturePartName
title: IXpsSigningOptions::GetSignaturePartName (xpsdigitalsignature.h)
description: Gets the part name of the document's signature part.
old-location: xps\ixpssigningoptions_getsignaturepartname.htm
tech.root: printdocs
ms.assetid: 8c5dfbda-0ceb-4694-bc5d-7e16e6f6d3bc
ms.date: 12/05/2018
ms.keywords: GetSignaturePartName, GetSignaturePartName method [XPS Documents and Packaging], GetSignaturePartName method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetSignaturePartName method, IXpsSigningOptions.GetSignaturePartName, IXpsSigningOptions::GetSignaturePartName, xps.ixpssigningoptions_getsignaturepartname, xpsdigitalsignature/IXpsSigningOptions::GetSignaturePartName
f1_keywords:
- xpsdigitalsignature/IXpsSigningOptions.GetSignaturePartName
dev_langs:
- c++
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
- IXpsSigningOptions.GetSignaturePartName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSigningOptions::GetSignaturePartName


## -description


Gets the part name of the document's signature part.


## -parameters




### -param signaturePartName [out, retval]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the document's signature part.

If a signature part name has not been set, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

