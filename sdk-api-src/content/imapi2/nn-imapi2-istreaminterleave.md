---
UID: NN:imapi2.IStreamInterleave
title: IStreamInterleave (imapi2.h)
description: Use this interface to combine several data streams into a single stream by alternately interspersing portions of each.
helpviewer_keywords: ["IStreamInterleave","IStreamInterleave interface [IMAPI]","IStreamInterleave interface [IMAPI]","described","imapi.istreaminterleave","imapi2/IStreamInterleave"]
old-location: imapi\istreaminterleave.htm
tech.root: imapi
ms.assetid: 2d0f03e5-a47d-4b46-a177-f462bbafe153
ms.date: 12/05/2018
ms.keywords: IStreamInterleave, IStreamInterleave interface [IMAPI], IStreamInterleave interface [IMAPI],described, imapi.istreaminterleave, imapi2/IStreamInterleave
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
 - IStreamInterleave
 - imapi2/IStreamInterleave
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
 - IStreamInterleave
---

# IStreamInterleave interface


## -description

Use this interface to combine several data streams into a single stream by alternately interspersing portions of each. You create interleaved streams when data streams need to run parallel to each other instead of sequentially. For example, some CD formats require user data interleaved with the subcode information. Any fixed-size interleave is supported.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftStreamInterleave) for the class identifier and __uuidof(IStreamInterleave) for the interface identifier.

## -inheritance

The <b>IStreamInterleave</b> interface inherits from <b>IStream</b>. <b>IStreamInterleave</b> also has these types of members:

## -remarks

To create the <b>MsftStreamInterleave</b> object in a script, use IMAPI2.MsftStreamInterleave as the program identifier when calling <b>CreateObject</b>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate">IStreamConcatenate</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased">IStreamPseudoRandomBased</a>
