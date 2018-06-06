---
UID: NF:uiautomationclient.IUIAutomation.CreateTreeWalker
title: IUIAutomation::CreateTreeWalker
author: windows-sdk-content
description: Retrieves a tree walker object that can be used to traverse the Microsoft UI Automation tree.
old-location: winauto\uiauto_IUIAutomation_CreateTreeWalker.htm
old-project: WinAuto
ms.assetid: c976bf97-656b-4992-b0c5-f442b501ad75
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: CreateTreeWalker, CreateTreeWalker method [Windows Accessibility], CreateTreeWalker method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateTreeWalker method, IUIAutomation.CreateTreeWalker, IUIAutomation::CreateTreeWalker, uiauto.uiauto_IUIAutomation_CreateTreeWalker, uiauto_IUIAutomation_CreateTreeWalker, uiautomationclient/IUIAutomation::CreateTreeWalker, winauto.uiauto_IUIAutomation_CreateTreeWalker
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.CreateTreeWalker
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation::CreateTreeWalker


## -description


Retrieves a tree walker object that can be used to traverse the Microsoft UI Automation tree.


## -parameters




### -param pCondition [in]

Type: <b><a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a>*</b>

A pointer to  a condition that specifies the elements of interest.


### -param walker [out, retval]

Type: <b><a href="https://msdn.microsoft.com/adb4afed-63b9-42b4-8a8d-673d4813bb52">IUIAutomationTreeWalker</a>**</b>

Receives a pointer to the tree walker object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



