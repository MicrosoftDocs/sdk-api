---
UID: NF:bits4_0.IBitsTokenOptions.ClearHelperToken
title: IBitsTokenOptions::ClearHelperToken (bits4_0.h)
description: Discards the helper token, and does not change the usage flags.
helpviewer_keywords: ["ClearHelperToken","ClearHelperToken method [BITS]","ClearHelperToken method [BITS]","IBitsTokenOptions interface","IBitsTokenOptions interface [BITS]","ClearHelperToken method","IBitsTokenOptions.ClearHelperToken","IBitsTokenOptions::ClearHelperToken","bits.ibitstokenoptions_clearhelpertoken","bits4_0/IBitsTokenOptions::ClearHelperToken"]
old-location: bits\ibitstokenoptions_clearhelpertoken.htm
tech.root: Bits
ms.assetid: 5af3496e-0792-46cc-bfc3-8ac6193724d1
ms.date: 12/05/2018
ms.keywords: ClearHelperToken, ClearHelperToken method [BITS], ClearHelperToken method [BITS],IBitsTokenOptions interface, IBitsTokenOptions interface [BITS],ClearHelperToken method, IBitsTokenOptions.ClearHelperToken, IBitsTokenOptions::ClearHelperToken, bits.ibitstokenoptions_clearhelpertoken, bits4_0/IBitsTokenOptions::ClearHelperToken
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
 - IBitsTokenOptions::ClearHelperToken
 - bits4_0/IBitsTokenOptions::ClearHelperToken
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
 - IBitsTokenOptions.ClearHelperToken
---

# IBitsTokenOptions::ClearHelperToken


## -description

Discards the helper token, and does not change the usage flags.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Older implementations effectively required that BITS users have  administrator privileges in order to clear a helper token with this method. Starting with Windows 10, version 1607, non-administrator BITS users can use this method to clear helper tokens on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="/windows/desktop/Services/networkservice-account">NetworkService account</a>) to use helper tokens effectively. 

Specifically, the implementation has been changed to allow users without administrator privileges to clear a helper token, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob::QueryInterface</a> call.

## -see-also

<a href="/windows/desktop/api/bits4_0/nn-bits4_0-ibitstokenoptions">IBitsTokenOptions</a>
