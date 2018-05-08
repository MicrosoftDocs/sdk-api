---
UID: NF:bits4_0.IBitsTokenOptions.ClearHelperToken
title: IBitsTokenOptions::ClearHelperToken
author: windows-driver-content
description: Discards the helper token, and does not change the usage flags.
old-location: bits\ibitstokenoptions_clearhelpertoken.htm
old-project: Bits
ms.assetid: 5af3496e-0792-46cc-bfc3-8ac6193724d1
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ClearHelperToken, ClearHelperToken method [BITS], ClearHelperToken method [BITS],IBitsTokenOptions interface, IBitsTokenOptions interface [BITS],ClearHelperToken method, IBitsTokenOptions.ClearHelperToken, IBitsTokenOptions::ClearHelperToken, bits.ibitstokenoptions_clearhelpertoken, bits4_0/IBitsTokenOptions::ClearHelperToken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits4_0.h
api_name:
-	IBitsTokenOptions.ClearHelperToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBitsTokenOptions::ClearHelperToken


## -description


Discards the helper token, and does not change the usage flags.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Older implementations effectively required that BITS users have  administrator privileges in order to clear a helper token with this method. Starting with Windows 10, version 1607, non-administrator BITS users can use this method to clear helper tokens on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="https://msdn.microsoft.com/f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7">NetworkService account</a>) to use helper tokens effectively. 

Specifically, the implementation has been changed to allow users without administrator privileges to clear a helper token, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob::QueryInterface</a> call.




## -see-also




<a href="https://msdn.microsoft.com/8496c27b-68d8-4709-b8a6-6ffa17c886df">IBitsTokenOptions</a>
 

 

