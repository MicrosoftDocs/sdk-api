---
UID: NF:uiautomationclient.IUIAutomation.CreateFalseCondition
title: IUIAutomation::CreateFalseCondition (uiautomationclient.h)
author: windows-sdk-content
description: Creates a condition that is always false.
old-location: winauto\uiauto_IUIAutomation_CreateFalseCondition.htm
tech.root: WinAuto
ms.assetid: 8fee46b7-a186-48b8-8fc0-f9844a2b6d8d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFalseCondition, CreateFalseCondition method [Windows Accessibility], CreateFalseCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateFalseCondition method, IUIAutomation.CreateFalseCondition, IUIAutomation::CreateFalseCondition, uiauto.uiauto_IUIAutomation_CreateFalseCondition, uiauto_IUIAutomation_CreateFalseCondition, uiautomationclient/IUIAutomation::CreateFalseCondition, winauto.uiauto_IUIAutomation_CreateFalseCondition
ms.topic: method
f1_keywords: 
 - "uiautomationclient/IUIAutomation.CreateFalseCondition"
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
 - IUIAutomation.CreateFalseCondition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::CreateFalseCondition


## -description


Creates a condition that is always false.


## -parameters




### -param newCondition [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the false condition.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method exists only for symmetry with <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createtruecondition">IUIAutomation::CreateTrueCondition</a>. A false condition will never enable a match with UI Automation elements, and it cannot usefully be combined with any other condition.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>
 

 

