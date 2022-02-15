---
UID: NN:imapi2.IStreamPseudoRandomBased
title: IStreamPseudoRandomBased (imapi2.h)
description: Use this interface to generate a read-only data stream whose data is initialized with pseudo-random data (not cryptographically safe). You must call the SetSize method to set the requested size of the stream.
helpviewer_keywords: ["IStreamPseudoRandomBased","IStreamPseudoRandomBased interface [IMAPI]","IStreamPseudoRandomBased interface [IMAPI]","described","imapi.istreampseudorandombased","imapi2/IStreamPseudoRandomBased"]
old-location: imapi\istreampseudorandombased.htm
tech.root: imapi
ms.assetid: 7630b8ac-41f9-4cc7-95e7-4172a876673f
ms.date: 12/05/2018
ms.keywords: IStreamPseudoRandomBased, IStreamPseudoRandomBased interface [IMAPI], IStreamPseudoRandomBased interface [IMAPI],described, imapi.istreampseudorandombased, imapi2/IStreamPseudoRandomBased
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IStreamPseudoRandomBased
 - imapi2/IStreamPseudoRandomBased
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IStreamPseudoRandomBased
---

# IStreamPseudoRandomBased interface


## -description

Use this interface to generate a read-only data stream whose data is initialized with pseudo-random data (not cryptographically safe). You must call the <b>SetSize</b> method to set the requested size of the stream.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use __uuidof(MsftStreamPrng001) for the class identifier and __uuidof(IStreamPseudoRandomBased) for the interface identifier.

## -inheritance

The <b>IStreamPseudoRandomBased</b> interface inherits from <b>IStream</b>. <b>IStreamPseudoRandomBased</b> also has these types of members:

## -remarks

To create the <b>MsftStreamPrgn001</b> object in a script, use IMAPI2.MsftStreamPrgn001 as the program identifier when calling <b>CreateObject</b>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate">IStreamConcatenate</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave">IStreamInterleave</a>
