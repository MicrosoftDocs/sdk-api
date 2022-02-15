---
UID: NN:bits4_0.IBitsTokenOptions
title: IBitsTokenOptions (bits4_0.h)
description: Use IBitsTokenOptions to associate and manage a pair of security tokens for a Background Intelligent Transfer Service (BITS) transfer job.
helpviewer_keywords: ["IBitsTokenOptions","IBitsTokenOptions interface [BITS]","IBitsTokenOptions interface [BITS]","described","bits.ibitstokenoptions","bits4_0/IBitsTokenOptions"]
old-location: bits\ibitstokenoptions.htm
tech.root: Bits
ms.assetid: 8496c27b-68d8-4709-b8a6-6ffa17c886df
ms.date: 12/05/2018
ms.keywords: IBitsTokenOptions, IBitsTokenOptions interface [BITS], IBitsTokenOptions interface [BITS],described, bits.ibitstokenoptions, bits4_0/IBitsTokenOptions
req.header: bits4_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits4_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on  Windows Vista with SP1,  Windows Vista with SP2, and  Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - IBitsTokenOptions
 - bits4_0/IBitsTokenOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits4_0.h
api_name:
 - IBitsTokenOptions
---

# IBitsTokenOptions interface


## -description

Use <b>IBitsTokenOptions</b> to associate and manage a pair of security tokens for a Background Intelligent Transfer Service (BITS) transfer job.

To get this interface, call the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob::QueryInterface</a> method, using __uuidof(IBitsTokenOptions) as the interface identifier.

## -inheritance

The <b>IBitsTokenOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBitsTokenOptions</b> also has these types of members:

