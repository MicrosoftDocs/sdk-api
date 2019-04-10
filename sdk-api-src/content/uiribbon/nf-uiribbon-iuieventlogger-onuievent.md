---
UID: NF:uiribbon.IUIEventLogger.OnUIEvent
title: IUIEventLogger::OnUIEvent (uiribbon.h)
author: windows-sdk-content
description: Receives notifications that a ribbon event has occurred.
old-location: windowsribbon\onuievent.htm
tech.root: windowsribbon
ms.assetid: 1BE6F914-C57D-4A8F-A286-C47BFD48B310
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIEventLogger interface [Windows Ribbon],OnUIEvent method, IUIEventLogger.OnUIEvent, IUIEventLogger::OnUIEvent, OnUIEvent, OnUIEvent method [Windows Ribbon], OnUIEvent method [Windows Ribbon],IUIEventLogger interface, uiribbon/IUIEventLogger::OnUIEvent, windowsribbon.onuievent
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.h
api_name:
 - IUIEventLogger.OnUIEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIEventLogger::OnUIEvent


## -description


Receives notifications that a ribbon event has occurred.


## -parameters




### -param pEventParams [in]

The parameters associated with the event. This value varies according to the event type.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54DB1BFF-0657-4027-8C8C-89CE998253F4">IUIEventLogger</a>



<a href="https://msdn.microsoft.com/EA278262-8CA7-42A3-9F66-0C7B4D3AA525">UI_EVENTLOCATION</a>



<a href="https://msdn.microsoft.com/438ACF91-3C83-4E2D-B919-4CCAE65BCD3E">UI_EVENTPARAMS</a>



<a href="https://msdn.microsoft.com/424C833C-E6D6-4532-8CF1-A294B429CC21">UI_EVENTTYPE</a>
 

 

