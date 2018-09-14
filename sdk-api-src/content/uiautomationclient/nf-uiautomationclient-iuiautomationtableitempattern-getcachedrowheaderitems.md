---
UID: NF:uiautomationclient.IUIAutomationTableItemPattern.GetCachedRowHeaderItems
title: IUIAutomationTableItemPattern::GetCachedRowHeaderItems
author: windows-sdk-content
description: Retrieves the cached row headers associated with a table item or cell.
old-location: winauto\uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems.htm
tech.root: WinAuto
ms.assetid: 69d4a632-8e35-4569-8c14-f56e9fd84c34
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetCachedRowHeaderItems, GetCachedRowHeaderItems method [Windows Accessibility], GetCachedRowHeaderItems method [Windows Accessibility],IUIAutomationTableItemPattern interface, IUIAutomationTableItemPattern interface [Windows Accessibility],GetCachedRowHeaderItems method, IUIAutomationTableItemPattern.GetCachedRowHeaderItems, IUIAutomationTableItemPattern::GetCachedRowHeaderItems, uiauto.uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems, uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems, uiautomationclient/IUIAutomationTableItemPattern::GetCachedRowHeaderItems, winauto.uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems
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
 - IUIAutomationTableItemPattern.GetCachedRowHeaderItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTableItemPattern::GetCachedRowHeaderItems


## -description


Retrieves the cached row headers associated with a table item or cell.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of cached row headers.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



