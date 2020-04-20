---
UID: NF:xpsdigitalsignature.IXpsSignatureBlockCollection.GetAt
title: IXpsSignatureBlockCollection::GetAt (xpsdigitalsignature.h)
description: Gets an IXpsSignatureBlock interface pointer from a specified location in the collection.helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsSignatureBlockCollection interface","IXpsSignatureBlockCollection interface [XPS Documents and Packaging]","GetAt method","IXpsSignatureBlockCollection.GetAt","IXpsSignatureBlockCollection::GetAt","xps.ixpssignatureblockcollection_getat","xpsdigitalsignature/IXpsSignatureBlockCollection::GetAt"]
old-location: xps\ixpssignatureblockcollection_getat.htm
tech.root: printdocs
ms.assetid: 4d3f89be-f9f3-46db-802f-ffb4867786c2
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsSignatureBlockCollection interface, IXpsSignatureBlockCollection interface [XPS Documents and Packaging],GetAt method, IXpsSignatureBlockCollection.GetAt, IXpsSignatureBlockCollection::GetAt, xps.ixpssignatureblockcollection_getat, xpsdigitalsignature/IXpsSignatureBlockCollection::GetAt
f1_keywords:
- xpsdigitalsignature/IXpsSignatureBlockCollection.GetAt
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
- IXpsSignatureBlockCollection.GetAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSignatureBlockCollection::GetAt


## -description


Gets an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer to be obtained.


### -param signatureBlock [out, retval]

The <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

