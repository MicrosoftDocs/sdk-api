---
UID: NF:uiautomationclient.IUIAutomation.CompareElements
title: IUIAutomation::CompareElements
author: windows-sdk-content
description: Compares two UI Automation elements to determine whether they represent the same underlying UI element.
old-location: winauto\uiauto_IUIAutomation_CompareElements.htm
old-project: WinAuto
ms.assetid: e4daa3c3-24fb-41df-a1b1-bd6545a47e51
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: CompareElements, CompareElements method [Windows Accessibility], CompareElements method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CompareElements method, IUIAutomation.CompareElements, IUIAutomation::CompareElements, uiauto.uiauto_IUIAutomation_CompareElements, uiauto_IUIAutomation_CompareElements, uiautomationclient/IUIAutomation::CompareElements, winauto.uiauto_IUIAutomation_CompareElements
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
 - IUIAutomation.CompareElements
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation::CompareElements


## -description


Compares two UI Automation elements to determine whether they represent the same underlying UI element.


## -parameters




### -param el1 [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the first element to compare.


### -param el2 [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the second element to compare.


### -param areSame [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Receives <b>TRUE</b> if the run-time identifiers of the elements are the same, or <b>FALSE</b> otherwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/b0c481eb-3545-439c-bf6a-347b98ea35de">IUIAutomation::CompareRuntimeIds</a>
 

 

