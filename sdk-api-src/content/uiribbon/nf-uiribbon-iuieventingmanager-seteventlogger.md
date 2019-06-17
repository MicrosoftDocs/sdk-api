---
UID: NF:uiribbon.IUIEventingManager.SetEventLogger
title: IUIEventingManager::SetEventLogger (uiribbon.h)
author: windows-sdk-content
description: Sets the event logger for ribbon events.
old-location: windowsribbon\iuieventingmanager_seteventlogger.htm
tech.root: windowsribbon
ms.assetid: C0228AB3-790A-469E-B185-06A26D02A96F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIEventingManager interface [Windows Ribbon],SetEventLogger method, IUIEventingManager.SetEventLogger, IUIEventingManager::SetEventLogger, SetEventLogger, SetEventLogger method [Windows Ribbon], SetEventLogger method [Windows Ribbon],IUIEventingManager interface, uiribbon/IUIEventingManager::SetEventLogger, windowsribbon.iuieventingmanager_seteventlogger
ms.topic: method
f1_keywords: ["uiribbon/IUIEventingManager.SetEventLogger"]
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUIEventingManager.SetEventLogger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIEventingManager::SetEventLogger


## -description


Sets the event logger for ribbon events.


## -parameters




### -param eventLogger [in]

The event logger.

If NULL, disables event logging.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize">IUIFramework::Initialize</a> and <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui">IUIFramework::LoadUI</a> before calling this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuieventlogger">IUIEventLogger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuieventingmanager">IUIEventingManager</a>
 

 

