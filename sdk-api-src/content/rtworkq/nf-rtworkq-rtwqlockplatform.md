---
UID: NF:rtworkq.RtwqLockPlatform
title: RtwqLockPlatform function
author: windows-sdk-content
description: Adds a reference to indicate to the platform that there are still pending asynchronous items. Blocks the RtwqShutdown function if there are active asynchronous items.
old-location: base\rtwqlockplatform.htm
old-project: procthread
ms.assetid: 25baa2ad-95b8-4ac0-a838-e95c6141e13b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: RtwqLockPlatform, RtwqLockPlatform function, base.rtwqlockplatform, rtworkq/RtwqLockPlatform
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
 - RtwqLockPlatform
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: ADAM
---

# RtwqLockPlatform function


## -description


Adds a reference to indicate to the platform that there are still pending asynchronous items. Blocks the <a href="https://msdn.microsoft.com/806c4142-b628-4ea0-b5e2-d2b4ead73c04">RtwqShutdown</a> function if there are active asynchronous items.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



