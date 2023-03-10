---
UID: NN:bits3_0.IBackgroundCopyJob4
title: IBackgroundCopyJob4 (bits3_0.h)
description: Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.
helpviewer_keywords: ["IBackgroundCopyJob4","IBackgroundCopyJob4 interface [BITS]","IBackgroundCopyJob4 interface [BITS]","described","bits.ibackgroundcopyjob4","bits3_0/IBackgroundCopyJob4"]
old-location: bits\ibackgroundcopyjob4.htm
tech.root: Bits
ms.assetid: 68909710-f749-487e-b064-9f8630929c53
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob4, IBackgroundCopyJob4 interface [BITS], IBackgroundCopyJob4 interface [BITS],described, bits.ibackgroundcopyjob4, bits3_0/IBackgroundCopyJob4
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 2.5 on  Windows Server 2003,  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob4
 - bits3_0/IBackgroundCopyJob4
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
 - IBackgroundCopyJob4
---

# IBackgroundCopyJob4 interface


## -description

Use this interface to enable peer caching, restrict download time, and inspect user token characteristics.

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob4)</code> as the interface identifier.

## -inheritance

The <b>IBackgroundCopyJob4</b> interface inherits from <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>, <a href="/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2">IBackgroundCopyJob2</a>, and <a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyjob3">IBackgroundCopyJob3</a>. <b>IBackgroundCopyJob4</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2">IBackgroundCopyJob2</a>



<a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyjob3">IBackgroundCopyJob3</a>
