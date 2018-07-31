---
UID: NF:uiautomationclient.IUIAutomationTextRange.Clone
title: IUIAutomationTextRange::Clone
author: windows-sdk-content
description: Retrieves a new IUIAutomationTextRange identical to the original and inheriting all properties of the original.
old-location: winauto\uiauto_IUIAutomationTextRange_Clone.htm
old-project: WinAuto
ms.assetid: 0f41fecf-fd66-443f-bc4d-23c05a4d3824
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Clone, Clone method [Windows Accessibility], Clone method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],Clone method, IUIAutomationTextRange.Clone, IUIAutomationTextRange::Clone, uiauto.uiauto_IUIAutomationTextRange_Clone, uiauto_IUIAutomationTextRange_Clone, uiautomationclient/IUIAutomationTextRange::Clone, winauto.uiauto_IUIAutomationTextRange_Clone
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
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRange::Clone


## -description


Retrieves a new <a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a> identical to the original and inheriting all properties of the original.


## -parameters




### -param clonedRange [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a pointer to the new text range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The new range can be manipulated independently of the original.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

