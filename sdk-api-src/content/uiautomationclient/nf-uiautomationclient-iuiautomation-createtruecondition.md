---
UID: NF:uiautomationclient.IUIAutomation.CreateTrueCondition
title: IUIAutomation::CreateTrueCondition (uiautomationclient.h)
description: Retrieves a predefined condition that selects all elements.helpviewer_keywords: ["CreateTrueCondition","CreateTrueCondition method [Windows Accessibility]","CreateTrueCondition method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateTrueCondition method","IUIAutomation.CreateTrueCondition","IUIAutomation::CreateTrueCondition","uiauto.uiauto_IUIAutomation_CreateTrueCondition","uiauto_IUIAutomation_CreateTrueCondition","uiautomationclient/IUIAutomation::CreateTrueCondition","winauto.uiauto_IUIAutomation_CreateTrueCondition"]
old-location: winauto\uiauto_IUIAutomation_CreateTrueCondition.htm
tech.root: WinAuto
ms.assetid: 02f55293-5d2d-4578-9c31-3ed04dac428e
ms.date: 12/05/2018
ms.keywords: CreateTrueCondition, CreateTrueCondition method [Windows Accessibility], CreateTrueCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateTrueCondition method, IUIAutomation.CreateTrueCondition, IUIAutomation::CreateTrueCondition, uiauto.uiauto_IUIAutomation_CreateTrueCondition, uiauto_IUIAutomation_CreateTrueCondition, uiautomationclient/IUIAutomation::CreateTrueCondition, winauto.uiauto_IUIAutomation_CreateTrueCondition
f1_keywords:
- uiautomationclient/IUIAutomation.CreateTrueCondition
dev_langs:
- c++
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
- IUIAutomation.CreateTrueCondition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::CreateTrueCondition


## -description


Retrieves a predefined condition that selects all elements.


## -parameters




### -param newCondition [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the true condition.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createfalsecondition">CreateFalseCondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>
 

 

