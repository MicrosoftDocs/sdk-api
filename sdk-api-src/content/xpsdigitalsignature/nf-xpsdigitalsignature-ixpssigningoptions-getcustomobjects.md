---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetCustomObjects
title: IXpsSigningOptions::GetCustomObjects (xpsdigitalsignature.h)
description: Gets a pointer to an IOpcSignatureCustomObjectSet interface that contains a set of signature custom objects.
helpviewer_keywords: ["GetCustomObjects","GetCustomObjects method [XPS Documents and Packaging]","GetCustomObjects method [XPS Documents and Packaging]","IXpsSigningOptions interface","IXpsSigningOptions interface [XPS Documents and Packaging]","GetCustomObjects method","IXpsSigningOptions.GetCustomObjects","IXpsSigningOptions::GetCustomObjects","xps.ixpssigningoptions_getcustomobjects","xpsdigitalsignature/IXpsSigningOptions::GetCustomObjects"]
old-location: xps\ixpssigningoptions_getcustomobjects.htm
tech.root: xps
ms.assetid: 17a3f913-57f2-40e1-b886-6cefb9e42a83
ms.date: 12/05/2018
ms.keywords: GetCustomObjects, GetCustomObjects method [XPS Documents and Packaging], GetCustomObjects method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetCustomObjects method, IXpsSigningOptions.GetCustomObjects, IXpsSigningOptions::GetCustomObjects, xps.ixpssigningoptions_getcustomobjects, xpsdigitalsignature/IXpsSigningOptions::GetCustomObjects
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
 - IXpsSigningOptions::GetCustomObjects
 - xpsdigitalsignature/IXpsSigningOptions::GetCustomObjects
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
 - IXpsSigningOptions.GetCustomObjects
---

# IXpsSigningOptions::GetCustomObjects


## -description

Gets a pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface that contains a set of signature custom objects.

## -parameters

### -param customObjectSet [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface that contains a set of signature custom objects.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The custom object set that this method returns is empty. To add  a custom object to this set, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobjectset-create">Create</a> method of the  interface that is returned in <i>customObjectSet</i>.

If a custom object must be signed, a reference to  that object  must be added  to the custom object set. For information on adding custom references, refer to  <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcustomreferences">GetCustomReferences</a>.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-getcustomreferences">GetCustomReferences</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>