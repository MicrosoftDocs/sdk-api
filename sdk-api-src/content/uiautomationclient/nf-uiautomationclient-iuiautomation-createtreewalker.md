---
UID: NF:uiautomationclient.IUIAutomation.CreateTreeWalker
title: IUIAutomation::CreateTreeWalker (uiautomationclient.h)
description: Retrieves a tree walker object that can be used to traverse the Microsoft UI Automation tree.
helpviewer_keywords: ["CreateTreeWalker","CreateTreeWalker method [Windows Accessibility]","CreateTreeWalker method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateTreeWalker method","IUIAutomation.CreateTreeWalker","IUIAutomation::CreateTreeWalker","uiauto.uiauto_IUIAutomation_CreateTreeWalker","uiauto_IUIAutomation_CreateTreeWalker","uiautomationclient/IUIAutomation::CreateTreeWalker","winauto.uiauto_IUIAutomation_CreateTreeWalker"]
old-location: winauto\uiauto_IUIAutomation_CreateTreeWalker.htm
tech.root: WinAuto
ms.assetid: c976bf97-656b-4992-b0c5-f442b501ad75
ms.date: 12/05/2018
ms.keywords: CreateTreeWalker, CreateTreeWalker method [Windows Accessibility], CreateTreeWalker method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateTreeWalker method, IUIAutomation.CreateTreeWalker, IUIAutomation::CreateTreeWalker, uiauto.uiauto_IUIAutomation_CreateTreeWalker, uiauto_IUIAutomation_CreateTreeWalker, uiautomationclient/IUIAutomation::CreateTreeWalker, winauto.uiauto_IUIAutomation_CreateTreeWalker
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation::CreateTreeWalker
 - uiautomationclient/IUIAutomation::CreateTreeWalker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.CreateTreeWalker
---

# IUIAutomation::CreateTreeWalker


## -description

Retrieves a tree walker object that can be used to traverse the Microsoft UI Automation tree.

## -parameters

### -param pCondition [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to  a condition that specifies the elements of interest.

### -param walker [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtreewalker">IUIAutomationTreeWalker</a>**</b>

Receives a pointer to the tree walker object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.