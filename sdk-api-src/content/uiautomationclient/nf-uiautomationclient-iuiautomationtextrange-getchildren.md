---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetChildren
title: IUIAutomationTextRange::GetChildren
author: windows-sdk-content
description: Retrieves a collection of all embedded objects that fall within the text range.
old-location: winauto\uiauto_IUIAutomationTextRange_GetChildren.htm
tech.root: WinAuto
ms.assetid: 714e9d91-c6b9-4fa2-8a14-9bdd721b3135
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetChildren method, IUIAutomationTextRange.GetChildren, IUIAutomationTextRange::GetChildren, uiauto.uiauto_IUIAutomationTextRange_GetChildren, uiauto_IUIAutomationTextRange_GetChildren, uiautomationclient/IUIAutomationTextRange::GetChildren, winauto.uiauto_IUIAutomationTextRange_GetChildren
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
 - IUIAutomationTextRange.GetChildren
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange::GetChildren


## -description


Retrieves a collection of all embedded objects that fall within the text range.


## -parameters




### -param children [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of all child objects that fall within the range. Children that overlap with the range but are not entirely enclosed by it are also included in the collection. An empty collection is returned if there are no child objects.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

