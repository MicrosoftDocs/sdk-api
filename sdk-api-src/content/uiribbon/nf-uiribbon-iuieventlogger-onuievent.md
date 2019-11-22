---
UID: NF:uiribbon.IUIEventLogger.OnUIEvent
title: IUIEventLogger::OnUIEvent (uiribbon.h)

description: Receives notifications that a ribbon event has occurred.
old-location: windowsribbon\onuievent.htm
tech.root: windowsribbon
ms.assetid: 1BE6F914-C57D-4A8F-A286-C47BFD48B310

ms.date: 12/05/2018
ms.keywords: IUIEventLogger interface [Windows Ribbon],OnUIEvent method, IUIEventLogger.OnUIEvent, IUIEventLogger::OnUIEvent, OnUIEvent, OnUIEvent method [Windows Ribbon], OnUIEvent method [Windows Ribbon],IUIEventLogger interface, uiribbon/IUIEventLogger::OnUIEvent, windowsribbon.onuievent
ms.topic: method
f1_keywords:
- uiribbon/IUIEventLogger.OnUIEvent
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuieventlogger">IUIEventLogger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventlocation">UI_EVENTLOCATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/ns-uiribbon-ui_eventparams">UI_EVENTPARAMS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventtype">UI_EVENTTYPE</a>
 

 

