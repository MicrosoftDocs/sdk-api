---
UID: NN:bits2_5.IBackgroundCopyJobHttpOptions
title: IBackgroundCopyJobHttpOptions (bits2_5.h)
description: Use this interface to specify client certificates for certificate-based client authentication and custom headers for HTTP requests.
helpviewer_keywords: ["IBackgroundCopyJobHttpOptions","IBackgroundCopyJobHttpOptions interface [BITS]","IBackgroundCopyJobHttpOptions interface [BITS]","described","bits.ibackgroundcopyjobhttpoptions","bits2_5/IBackgroundCopyJobHttpOptions"]
old-location: bits\ibackgroundcopyjobhttpoptions.htm
tech.root: Bits
ms.assetid: d8ccf65d-a4f1-44d9-9903-43e5529f1f29
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJobHttpOptions, IBackgroundCopyJobHttpOptions interface [BITS], IBackgroundCopyJobHttpOptions interface [BITS],described, bits.ibackgroundcopyjobhttpoptions, bits2_5/IBackgroundCopyJobHttpOptions
req.header: bits2_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJobHttpOptions
 - bits2_5/IBackgroundCopyJobHttpOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx4.dll
api_name:
 - IBackgroundCopyJobHttpOptions
---

# IBackgroundCopyJobHttpOptions interface


## -description

Use this interface to specify client certificates for certificate-based client authentication and custom headers for HTTP requests. 

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using __uuidof(IBackgroundCopyJobHttpOptions) for the interface identifier.

## -inheritance

The <b>IBackgroundCopyJobHttpOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyJobHttpOptions</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>
