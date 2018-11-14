---
UID: NF:uiautomationclient.IUIAutomationSelectionPattern.GetCachedSelection
title: IUIAutomationSelectionPattern::GetCachedSelection
author: windows-sdk-content
description: Retrieves the cached selected elements in the container.
old-location: winauto\uiauto_IUIAutomationSelectionPattern_GetCachedSelection.htm
tech.root: WinAuto
ms.assetid: a0f2d198-78a9-4117-9a55-aa9042ef3f21
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCachedSelection, GetCachedSelection method [Windows Accessibility], GetCachedSelection method [Windows Accessibility],IUIAutomationSelectionPattern interface, IUIAutomationSelectionPattern interface [Windows Accessibility],GetCachedSelection method, IUIAutomationSelectionPattern.GetCachedSelection, IUIAutomationSelectionPattern::GetCachedSelection, uiauto.uiauto_IUIAutomationSelectionPattern_GetCachedSelection, uiauto_IUIAutomationSelectionPattern_GetCachedSelection, uiautomationclient/IUIAutomationSelectionPattern::GetCachedSelection, winauto.uiauto_IUIAutomationSelectionPattern_GetCachedSelection
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
 - IUIAutomationSelectionPattern.GetCachedSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomationSelectionPattern.GetCachedSelection
: 
---

# IUIAutomationSelectionPattern::GetCachedSelection


## -description


Retrieves the cached selected elements in the container.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to the cached collection of selected elements. The default is an empty array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/10e0c9c3-ed42-4ffa-b0a8-25a1c760a583">IUIAutomationSelectionPattern</a>
 

 

