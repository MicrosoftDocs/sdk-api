---
UID: NF:uiautomationcore.ISynchronizedInputProvider.StartListening
title: ISynchronizedInputProvider::StartListening
author: windows-sdk-content
description: Starts listening for input of the specified type.
old-location: winauto\uiauto_ISynchronizedInputProvider_StartListening.htm
old-project: WinAuto
ms.assetid: ad9e6ca3-b38c-41f8-9c61-ce51786672eb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISynchronizedInputProvider interface [Windows Accessibility],StartListening method, ISynchronizedInputProvider.StartListening, ISynchronizedInputProvider::StartListening, StartListening, StartListening method [Windows Accessibility], StartListening method [Windows Accessibility],ISynchronizedInputProvider interface, uiauto.uiauto_ISynchronizedInputProvider_StartListening, uiauto_ISynchronizedInputProvider_StartListening, uiautomationcore/ISynchronizedInputProvider::StartListening, winauto.uiauto_ISynchronizedInputProvider_StartListening
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ISynchronizedInputProvider.StartListening
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISynchronizedInputProvider::StartListening


## -description


Starts listening for input of the specified type. 


## -parameters




### -param inputType [in]

Type: <b><a href="https://msdn.microsoft.com/28c66392-89f0-40eb-be19-ac84c64dacb7">SynchronizedInputType</a></b>

The type of input that is requested to be synchronized. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When it finds matching input, the provider checks if the target UI Automation element matches the current element. If they match, the provider raises the <a href="https://msdn.microsoft.com/en-us/library/Ee671223(v=VS.85).aspx">UIA_InputReachedTargetEventId</a> event; otherwise, it raises the <a href="https://msdn.microsoft.com/en-us/library/Ee671223(v=VS.85).aspx">UIA_InputReachedOtherElementEventId</a>  or <a href="https://msdn.microsoft.com/en-us/library/Ee671223(v=VS.85).aspx">UIA_InputDiscardedEventId</a> event. The UI Automation provider must discard the input if it is for an element other than this one.

This is a one-shot method; after receiving input, the provider stops listening and continues normally.

This method returns E_INVALIDOPERATION if the provider is already listening for input.




## -see-also




<a href="https://msdn.microsoft.com/70495eba-172a-432e-951d-1092fd676d5e">ISynchronizedInputProvider</a>
 

 

