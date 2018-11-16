---
UID: NF:uiautomationclient.IUIAutomationTextRange.FindText
title: IUIAutomationTextRange::FindText
author: windows-sdk-content
description: Retrieves a text range subset that contains the specified text.
old-location: winauto\uiauto_IUIAutomationTextRange_FindText.htm
tech.root: WinAuto
ms.assetid: 1d6e9216-747b-45b5-90ac-ec19d36e5a0a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FindText, FindText method [Windows Accessibility], FindText method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],FindText method, IUIAutomationTextRange.FindText, IUIAutomationTextRange::FindText, uiauto.uiauto_IUIAutomationTextRange_FindText, uiauto_IUIAutomationTextRange_FindText, uiautomationclient/IUIAutomationTextRange::FindText, winauto.uiauto_IUIAutomationTextRange_FindText
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
 - IUIAutomationTextRange.FindText
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
- IUIAutomationTextRange.FindText
: 
---

# IUIAutomationTextRange::FindText


## -description


Retrieves a text range subset that contains the specified text. 


## -parameters




### -param text [in]

Type: <b>BSTR</b>

The text to find.


### -param backward [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>.


### -param ignoreCase [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if case should be ignored; otherwise <b>FALSE</b>.


### -param found [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a pointer to the text range, or <b>NULL</b> if no match is found.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There is no differentiation between hidden and visible text.
             




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

