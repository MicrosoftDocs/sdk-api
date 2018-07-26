---
UID: NF:uiautomationclient.IUIAutomationElement.GetCurrentPatternAs
title: IUIAutomationElement::GetCurrentPatternAs
author: windows-sdk-content
description: Retrieves the control pattern interface of the specified pattern on this UI Automation element.
old-location: winauto\uiauto_IUIAutomationElement_GetCurrentPatternAs.htm
old-project: WinAuto
ms.assetid: 98b0f647-7f6e-4e07-8530-1dae781507bc
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetCurrentPatternAs, GetCurrentPatternAs method [Windows Accessibility], GetCurrentPatternAs method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCurrentPatternAs method, IUIAutomationElement.GetCurrentPatternAs, IUIAutomationElement::GetCurrentPatternAs, uiauto.uiauto_IUIAutomationElement_GetCurrentPatternAs, uiauto_IUIAutomationElement_GetCurrentPatternAs, uiautomationclient/IUIAutomationElement::GetCurrentPatternAs, winauto.uiauto_IUIAutomationElement_GetCurrentPatternAs
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
 - IUIAutomationElement.GetCurrentPatternAs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElement::GetCurrentPatternAs


## -description


Retrieves the control pattern interface of the specified pattern on this UI Automation element.


## -parameters




### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="https://msdn.microsoft.com/0192e840-96e6-4b12-a570-0d33a36ed885">Control Pattern Identifiers</a>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.


### -param patternObject






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



<a href="https://msdn.microsoft.com/2d0170e2-277e-48f8-a2e4-5c4ece92d8ec">GetCachedPatternAs</a>



<a href="https://msdn.microsoft.com/3ad4df7c-979d-464f-9600-d1f3de064b59">GetCurrentPattern</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/fdac2b9f-916a-495a-b187-c4d8086319ff">UI Automation Control Patterns Overview</a>
 

 

