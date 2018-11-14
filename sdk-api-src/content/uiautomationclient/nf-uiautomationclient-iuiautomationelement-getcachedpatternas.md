---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedPatternAs
title: IUIAutomationElement::GetCachedPatternAs
author: windows-sdk-content
description: Retrieves the control pattern interface of the specified pattern from the cache of this UI Automation element.
old-location: winauto\uiauto_IUIAutomationElement_GetCachedPatternAs.htm
tech.root: WinAuto
ms.assetid: 2d0170e2-277e-48f8-a2e4-5c4ece92d8ec
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCachedPatternAs, GetCachedPatternAs method [Windows Accessibility], GetCachedPatternAs method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedPatternAs method, IUIAutomationElement.GetCachedPatternAs, IUIAutomationElement::GetCachedPatternAs, uiauto.uiauto_IUIAutomationElement_GetCachedPatternAs, uiauto_IUIAutomationElement_GetCachedPatternAs, uiautomationclient/IUIAutomationElement::GetCachedPatternAs, winauto.uiauto_IUIAutomationElement_GetCachedPatternAs
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
 - IUIAutomationElement.GetCachedPatternAs
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
- IUIAutomationElement.GetCachedPatternAs
: 
---

# IUIAutomationElement::GetCachedPatternAs


## -description


Retrieves the control pattern interface of the specified pattern from the cache of this UI Automation element.


## -parameters




### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="https://msdn.microsoft.com/0192e840-96e6-4b12-a570-0d33a36ed885">Control Pattern Identifiers</a>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.


### -param patternObject

TBD




#### - ppv [out]

Type: <b>void**</b>

Receives the interface pointer requested in <i>riid</i>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/c71cab11-24c7-4e66-bcf2-f1abb1f37abb">GetCachedPattern</a>



<a href="https://msdn.microsoft.com/98b0f647-7f6e-4e07-8530-1dae781507bc">GetCurrentPatternAs</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/fdac2b9f-916a-495a-b187-c4d8086319ff">UI Automation Control Patterns Overview</a>
 

 

