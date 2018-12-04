---
UID: NF:mfidl.MFCreatePresentationClock
title: MFCreatePresentationClock function
author: windows-sdk-content
description: Creates the presentation clock.
old-location: mf\mfcreatepresentationclock.htm
tech.root: medfound
ms.assetid: b0ed3482-d127-45d3-a4de-271b1c0a199b
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: MFCreatePresentationClock, MFCreatePresentationClock function [Media Foundation], b0ed3482-d127-45d3-a4de-271b1c0a199b, mf.mfcreatepresentationclock, mfidl/MFCreatePresentationClock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreatePresentationClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreatePresentationClock function


## -description


Creates the presentation clock. The presentation clock is used to schedule the time at which samples are rendered and to synchronize multiple streams.



## -parameters




### -param ppPresentationClock

Receives a pointer to the clock's <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller must shut down the presentation clock by calling <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">IMFShutdown::Shutdown</a> on the clock.

Typically applications do not create the presentation clock. The Media Session automatically creates the presentation clock. To get a pointer to the presentation clock from the Media Session, call <a href="https://msdn.microsoft.com/16444da2-68f2-4d94-8c6f-9e512d51e5e9">IMFMediaSession::GetClock</a>.




## -see-also




<a href="https://msdn.microsoft.com/09f50b11-0e0a-42b6-a7bf-bb0135343351">About the Media Session</a>



<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

