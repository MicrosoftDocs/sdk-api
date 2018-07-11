---
UID: NF:rtworkq.RtwqUnlockPlatform
title: RtwqUnlockPlatform function
author: windows-sdk-content
description: Unlocks the platform after it was locked by a call to the RtwqLockPlatform function.
old-location: base\rtwqunlockplatform.htm
old-project: ProcThread
ms.assetid: 8f1e00fb-863a-49e6-a0e3-a3491637b47b
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: RtwqUnlockPlatform, RtwqUnlockPlatform function, base.rtwqunlockplatform, rtworkq/RtwqUnlockPlatform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqUnlockPlatform
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: ADAM
---

# RtwqUnlockPlatform function


## -description


Unlocks the platform after it was locked by a call to the <a href="https://msdn.microsoft.com/25baa2ad-95b8-4ac0-a838-e95c6141e13b">RtwqLockPlatform</a> function.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



