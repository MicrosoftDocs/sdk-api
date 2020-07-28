---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetSignaturePartName
title: IXpsSigningOptions::SetSignaturePartName (xpsdigitalsignature.h)
description: Sets the part name of the document's signature part.
helpviewer_keywords: ["IXpsSigningOptions interface [XPS Documents and Packaging]","SetSignaturePartName method","IXpsSigningOptions.SetSignaturePartName","IXpsSigningOptions::SetSignaturePartName","SetSignaturePartName","SetSignaturePartName method [XPS Documents and Packaging]","SetSignaturePartName method [XPS Documents and Packaging]","IXpsSigningOptions interface","xps.ixpssigningoptions_setsignaturepartname","xpsdigitalsignature/IXpsSigningOptions::SetSignaturePartName"]
old-location: xps\ixpssigningoptions_setsignaturepartname.htm
tech.root: xps
ms.assetid: 24addd5c-09a5-4f1b-90eb-c398aa7dd9a1
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetSignaturePartName method, IXpsSigningOptions.SetSignaturePartName, IXpsSigningOptions::SetSignaturePartName, SetSignaturePartName, SetSignaturePartName method [XPS Documents and Packaging], SetSignaturePartName method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setsignaturepartname, xpsdigitalsignature/IXpsSigningOptions::SetSignaturePartName
f1_keywords:
- xpsdigitalsignature/IXpsSigningOptions.SetSignaturePartName
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
- IXpsSigningOptions.SetSignaturePartName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSigningOptions::SetSignaturePartName


## -description


Sets the part name of the document's signature part.


## -parameters




### -param signaturePartName [in]

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the document's signature part.

If this parameter is <b>NULL</b>, this method will generate a random, unique part name for the signature part.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

