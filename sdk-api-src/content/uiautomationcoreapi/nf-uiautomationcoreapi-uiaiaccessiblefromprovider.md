---
UID: NF:uiautomationcoreapi.UiaIAccessibleFromProvider
title: UiaIAccessibleFromProvider function
author: windows-sdk-content
description: Retrieves an IAccessible implementation that provides Microsoft Active Accessibility data on behalf of a Microsoft UI Automation provider.
old-location: winauto\uiauto_UiaIAccessibleFromProvider.htm
tech.root: WinAuto
ms.assetid: 79523637-9858-4E0B-87E7-8CED19FADF0E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UIA_IAFP_DEFAULT, UIA_IAFP_UNWRAP_BRIDGE, UiaIAccessibleFromProvider, UiaIAccessibleFromProvider function [Windows Accessibility], uiautomationcoreapi/UiaIAccessibleFromProvider, winauto.uiauto_UiaIAccessibleFromProvider
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaIAccessibleFromProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaIAccessibleFromProvider function


## -description


Retrieves an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> implementation that provides Microsoft Active Accessibility data on behalf of a Microsoft UI Automation provider.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

A pointer to the UI Automation object.


### -param dwFlags [in]

Type: <b>DWORD</b>


One of the following values:



<a id="UIA_IAFP_DEFAULT"></a>
<a id="uia_iafp_default"></a>


#### UIA_IAFP_DEFAULT

<a id="UIA_IAFP_UNWRAP_BRIDGE"></a>
<a id="uia_iafp_unwrap_bridge"></a>


#### UIA_IAFP_UNWRAP_BRIDGE


### -param ppAccessible [out]

Type: <b><a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>**</b>

Receives the pointer to the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> implementation for the provider.


### -param pvarChild [out]

Type: <b><a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a>*</b>

Receives the child identifier of the accessible element in the <b>lVal</b> member.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In most cases, this function retrieves a wrapper object, provided by Windows, that implements <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> on behalf of the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> object.  If the provided <b>IRawElementProviderSimple</b> pointer is itself a wrapper object, this function retrieves the wrapped <b>IAccessible</b> pointer and returns that instead, to prevent the creation of multiple layers of wrappers.




## -see-also




<a href="https://msdn.microsoft.com/76012ec7-0114-4b6b-a35e-5cfde5b90230">Functions for Providers</a>



<a href="https://msdn.microsoft.com/9858B3B2-CE93-4209-BAFE-BFC911042800">UiaProviderFromIAccessible</a>
 

 

