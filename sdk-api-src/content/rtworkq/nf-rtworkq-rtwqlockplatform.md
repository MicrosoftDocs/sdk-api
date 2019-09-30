---
UID: NF:rtworkq.RtwqLockPlatform
title: RtwqLockPlatform function (rtworkq.h)
author: windows-sdk-content
description: Adds a reference to indicate to the platform that there are still pending asynchronous items. Blocks the RtwqShutdown function if there are active asynchronous items.
old-location: base\rtwqlockplatform.htm
tech.root: ProcThread
ms.assetid: 25baa2ad-95b8-4ac0-a838-e95c6141e13b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtwqLockPlatform, RtwqLockPlatform function, base.rtwqlockplatform, rtworkq/RtwqLockPlatform
ms.topic: function
f1_keywords: 
 - "rtworkq/RtwqLockPlatform"
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
 - RtwqLockPlatform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtwqLockPlatform function


## -description


Adds a reference to indicate to the platform that there are still pending asynchronous items. Blocks the <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqshutdown">RtwqShutdown</a> function if there are active asynchronous items.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



