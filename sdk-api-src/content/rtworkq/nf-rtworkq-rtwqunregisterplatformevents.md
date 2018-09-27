---
UID: NF:rtworkq.RtwqUnregisterPlatformEvents
title: RtwqUnregisterPlatformEvents function
author: windows-sdk-content
description: Unregisters a listener event from the callback platform.
old-location: base\rtwqunregisterplatformevents.htm
tech.root: procthread
ms.assetid: C1AB42C4-745B-46D6-9A1C-B5FD2443F48B
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: RtwqUnregisterPlatformEvents, RtwqUnregisterPlatformEvents function, base.rtwqunregisterplatformevents, rtworkq/RtwqUnregisterPlatformEvents
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - RtwqUnregisterPlatformEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqUnregisterPlatformEvents function


## -description


Unregisters a listener event from the callback platform.


## -parameters




### -param platformEvents

Pointer to the <a href="https://msdn.microsoft.com/9184D930-9305-4CA0-8E89-0CBAA5E4D53F">IRtwqPlatformEvents</a>  object which provides the events.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The app should use the same pointer that was passed to <a href="base.rtwqregisterplatformextension">RtwqRegisterPlatformExtension</a>.



