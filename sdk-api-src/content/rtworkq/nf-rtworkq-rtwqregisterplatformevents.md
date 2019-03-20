---
UID: NF:rtworkq.RtwqRegisterPlatformEvents
title: RtwqRegisterPlatformEvents function (rtworkq.h)
author: windows-sdk-content
description: Enables an app to listen to the RtwqStartup and RtwqShutdown functions.
old-location: base\rtwqregisterplatformevents.htm
tech.root: ProcThread
ms.assetid: 7BD7E83B-29E1-4FF5-B527-71C2F80D6521
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtwqRegisterPlatformEvents, RtwqRegisterPlatformEvents function, base.rtwqregisterplatformevents, rtworkq/RtwqRegisterPlatformEvents
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
 - RtwqRegisterPlatformEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqRegisterPlatformEvents function


## -description


Enables an app to listen to the <a href="https://msdn.microsoft.com/101e73ec-34ec-49af-999d-5410f46ff319">RtwqStartup</a> and <a href="https://msdn.microsoft.com/806c4142-b628-4ea0-b5e2-d2b4ead73c04">RtwqShutdown</a> functions.


## -parameters




### -param platformEvents [in]

Pointer to the <a href="https://msdn.microsoft.com/9184D930-9305-4CA0-8E89-0CBAA5E4D53F">IRtwqPlatformEvents</a>  object which provides the events.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



