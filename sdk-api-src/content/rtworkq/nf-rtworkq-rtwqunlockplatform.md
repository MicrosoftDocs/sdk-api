---
UID: NF:rtworkq.RtwqUnlockPlatform
title: RtwqUnlockPlatform function (rtworkq.h)
description: Unlocks the platform after it was locked by a call to the RtwqLockPlatform function.
helpviewer_keywords: ["RtwqUnlockPlatform","RtwqUnlockPlatform function","base.rtwqunlockplatform","rtworkq/RtwqUnlockPlatform"]
old-location: base\rtwqunlockplatform.htm
tech.root: backup
ms.assetid: 8f1e00fb-863a-49e6-a0e3-a3491637b47b
ms.date: 12/05/2018
ms.keywords: RtwqUnlockPlatform, RtwqUnlockPlatform function, base.rtwqunlockplatform, rtworkq/RtwqUnlockPlatform
f1_keywords:
- rtworkq/RtwqUnlockPlatform
dev_langs:
- c++
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- RTWorkQ.dll
api_name:
- RtwqUnlockPlatform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtwqUnlockPlatform function


## -description


Unlocks the platform after it was locked by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqlockplatform">RtwqLockPlatform</a> function.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



