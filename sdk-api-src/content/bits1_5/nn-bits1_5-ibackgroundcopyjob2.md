---
UID: NN:bits1_5.IBackgroundCopyJob2
title: IBackgroundCopyJob2
description: Retrieve reply data from an upload-reply job, determine the progress of the reply data transfer to the client, request command line execution, and provide credentials for proxy and remote server authentication requests.
helpviewer_keywords: ["IBackgroundCopyJob2","IBackgroundCopyJob2 interface [BITS]","IBackgroundCopyJob2 interface [BITS]","described","_drz_ibackgroundcopyjob2","bits.ibackgroundcopyjob2","bits1_5/IBackgroundCopyJob2"]
old-location: bits\ibackgroundcopyjob2.htm
tech.root: Bits
ms.assetid: 9fd422ba-a68c-40e3-8b21-3077b271e58e
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob2, IBackgroundCopyJob2 interface [BITS], IBackgroundCopyJob2 interface [BITS],described, _drz_ibackgroundcopyjob2, bits.ibackgroundcopyjob2, bits1_5/IBackgroundCopyJob2
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob2
 - bits1_5/IBackgroundCopyJob2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2
---

# IBackgroundCopyJob2 interface


## -description

Use the 
<b>IBackgroundCopyJob2</b> interface to retrieve reply data from an upload-reply job, determine the progress of the reply data transfer to the client, request command line execution, and provide credentials for proxy and remote server authentication requests.

The 
<b>IBackgroundCopyJob2</b> interface inherits from the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface. 

To get an 
<b>IBackgroundCopyJob2</b> interface pointer, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob2)</code> for the interface identifier. Use the 
<b>IBackgroundCopyJob2</b> interface pointer to call both the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> and 
<b>IBackgroundCopyJob2</b> methods.

## -inheritance

The <b>IBackgroundCopyJob2</b> interface inherits from <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>. <b>IBackgroundCopyJob2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>
