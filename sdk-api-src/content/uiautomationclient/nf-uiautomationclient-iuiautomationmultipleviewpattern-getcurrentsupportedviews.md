---
UID: NF:uiautomationclient.IUIAutomationMultipleViewPattern.GetCurrentSupportedViews
title: IUIAutomationMultipleViewPattern::GetCurrentSupportedViews
author: windows-sdk-content
description: Retrieves a collection of control-specific view identifiers.
old-location: winauto\uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews.htm
tech.root: WinAuto
ms.assetid: 9380797a-b546-4e36-9403-d34cea672ace
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetCurrentSupportedViews, GetCurrentSupportedViews method [Windows Accessibility], GetCurrentSupportedViews method [Windows Accessibility],IUIAutomationMultipleViewPattern interface, IUIAutomationMultipleViewPattern interface [Windows Accessibility],GetCurrentSupportedViews method, IUIAutomationMultipleViewPattern.GetCurrentSupportedViews, IUIAutomationMultipleViewPattern::GetCurrentSupportedViews, uiauto.uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews, uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews, uiautomationclient/IUIAutomationMultipleViewPattern::GetCurrentSupportedViews, winauto.uiauto_IUIAutomationMultipleViewPattern_GetCurrentSupportedViews
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - UIAutomationClient.h
api_name:
 - IUIAutomationMultipleViewPattern.GetCurrentSupportedViews
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationMultipleViewPattern::GetCurrentSupportedViews


## -description


Retrieves a collection of control-specific view identifiers.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to an array of view identifiers.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<a href="https://msdn.microsoft.com/4a1613b9-1e64-4d4e-876e-e2bf886097d4">IUIAutomationMultipleViewPattern</a>
 

 

