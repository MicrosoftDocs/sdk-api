---
UID: NF:uiautomationcore.IRawElementProviderSimple.GetPatternProvider
title: IRawElementProviderSimple::GetPatternProvider
author: windows-sdk-content
description: Retrieves a pointer to an object that provides support for a control pattern on a Microsoft UI Automation element.
old-location: winauto\uiauto_IRawElementProviderSimple_GetPatternProvider.htm
tech.root: WinAuto
ms.assetid: 8315c1d4-6347-462f-9c96-121f216faf88
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetPatternProvider, GetPatternProvider method [Windows Accessibility], GetPatternProvider method [Windows Accessibility],IRawElementProviderSimple interface, IRawElementProviderSimple interface [Windows Accessibility],GetPatternProvider method, IRawElementProviderSimple.GetPatternProvider, IRawElementProviderSimple::GetPatternProvider, uiauto.uiauto_IRawElementProviderSimple_GetPatternProvider, uiauto_IRawElementProviderSimple_GetPatternProvider, uiautomationcore/IRawElementProviderSimple::GetPatternProvider, winauto.uiauto_IRawElementProviderSimple_GetPatternProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - UIAutomationCore.h
api_name:
 - IRawElementProviderSimple.GetPatternProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationcore.h
: 
- IRawElementProviderSimple.GetPatternProvider
: 
---

# IRawElementProviderSimple::GetPatternProvider


## -description


Retrieves a pointer to an object that provides support for a control pattern on a Microsoft UI Automation element.


## -parameters




### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="https://msdn.microsoft.com/0192e840-96e6-4b12-a570-0d33a36ed885">Control Pattern Identifiers</a>.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives a pointer to the object that supports the control pattern,
				or <b>NULL</b> if the control pattern is not supported. 
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>
 

 

