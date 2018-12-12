---
UID: NF:uiribbon.IUIEventingManager.SetEventLogger
title: IUIEventingManager::SetEventLogger
author: windows-sdk-content
description: Sets the event logger for ribbon events.
old-location: windowsribbon\iuieventingmanager_seteventlogger.htm
tech.root: windowsribbon
ms.assetid: C0228AB3-790A-469E-B185-06A26D02A96F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIEventingManager interface [Windows Ribbon],SetEventLogger method, IUIEventingManager.SetEventLogger, IUIEventingManager::SetEventLogger, SetEventLogger, SetEventLogger method [Windows Ribbon], SetEventLogger method [Windows Ribbon],IUIEventingManager interface, uiribbon/IUIEventingManager::SetEventLogger, windowsribbon.iuieventingmanager_seteventlogger
ms.prod: windows-hardware
ms.technology: windows-devices
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



Call <a href="https://msdn.microsoft.com/en-us/library/Dd371373(v=VS.85).aspx">IUIFramework::Initialize</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd371471(v=VS.85).aspx">IUIFramework::LoadUI</a> before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/54DB1BFF-0657-4027-8C8C-89CE998253F4">IUIEventLogger</a>



<a href="https://msdn.microsoft.com/11E53D75-B8C0-40A3-8E4D-ACAA10BEAC84">IUIEventingManager</a>
 

 

