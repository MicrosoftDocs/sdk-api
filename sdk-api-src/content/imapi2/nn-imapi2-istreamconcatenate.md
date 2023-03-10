---
UID: NN:imapi2.IStreamConcatenate
title: IStreamConcatenate (imapi2.h)
description: Use this interface to combine several data streams into a single stream.
helpviewer_keywords: ["IStreamConcatenate","IStreamConcatenate interface [IMAPI]","IStreamConcatenate interface [IMAPI]","described","imapi.istreamconcatenate","imapi2/IStreamConcatenate"]
old-location: imapi\istreamconcatenate.htm
tech.root: imapi
ms.assetid: 48b786ef-a1b6-4dcf-9329-c659f15185e1
ms.date: 12/05/2018
ms.keywords: IStreamConcatenate, IStreamConcatenate interface [IMAPI], IStreamConcatenate interface [IMAPI],described, imapi.istreamconcatenate, imapi2/IStreamConcatenate
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
 - IStreamConcatenate
 - imapi2/IStreamConcatenate
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
 - IStreamConcatenate
---

# IStreamConcatenate interface


## -description

Use this interface to combine several data streams into a single stream.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftStreamConcatenate) for the class identifier and __uuidof(IStreamConcatenate) for the interface identifier.

## -inheritance

The <b>IStreamConcatenate</b> interface inherits from <b>IStream</b>. <b>IStreamConcatenate</b> also has these types of members:

## -remarks

To create the  MsftStreamConcatenate object in a script, use IMAPI2.MsftStreamConcatenate as the program identifier when calling CreateObject.

When using this interface, the following  scenarios will result in undefined behaviors, and should be avoided:

<ul>
<li>Each partial stream composing the MsftStreamConcatenate object is actually the same stream.</li>
<li>Any of the concatenated streams are modified (read from, written to, or seeked on) outside of IMAPI.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave">IStreamInterleave</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased">IStreamPseudoRandomBased</a>
