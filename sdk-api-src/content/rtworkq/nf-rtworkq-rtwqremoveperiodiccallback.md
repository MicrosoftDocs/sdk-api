---
UID: NF:rtworkq.RtwqRemovePeriodicCallback
title: RtwqRemovePeriodicCallback function (rtworkq.h)
author: windows-sdk-content
description: Cancels a callback function that was set by the RtwqAddPeriodicCallback function.
old-location: base\rtwqremoveperiodiccallback.htm
tech.root: ProcThread
ms.assetid: 308910e3-dae8-4f23-9782-adf2996a58aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtwqRemovePeriodicCallback, RtwqRemovePeriodicCallback function, base.rtwqremoveperiodiccallback, rtworkq/RtwqRemovePeriodicCallback
ms.topic: function
f1_keywords: 
 - "rtworkq/RtwqRemovePeriodicCallback"
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
 - RtwqRemovePeriodicCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtwqRemovePeriodicCallback function


## -description



Cancels a callback function that was set by the <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqaddperiodiccallback">RtwqAddPeriodicCallback</a> function.




## -parameters




### -param dwKey [in]

Key that identifies the callback. This value is retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqaddperiodiccallback">RtwqAddPeriodicCallback</a> function.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



