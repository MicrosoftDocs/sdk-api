---
UID: NF:uiautomationcoreapi.UiaProviderFromIAccessible
title: UiaProviderFromIAccessible function
author: windows-sdk-content
description: Creates a Microsoft UI Automation provider based on the specified Microsoft Active Accessibility object.
old-location: winauto\uiauto_UiaProviderFromIAccessibleFunction.htm
tech.root: WinAuto
ms.assetid: 9858B3B2-CE93-4209-BAFE-BFC911042800
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: UIA_PFIA_DEFAULT, UIA_PFIA_UNWRAP_BRIDGE, UiaProviderFromIAccessible, UiaProviderFromIAccessible function [Windows Accessibility], uiautomationcoreapi/UiaProviderFromIAccessible, winauto.uiauto_UiaProviderFromIAccessibleFunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - UiaProviderFromIAccessible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaProviderFromIAccessible function


## -description


Creates a Microsoft UI Automation provider based on the specified Microsoft Active Accessibility object.


## -parameters




### -param pAccessible [in]

Type: <b><a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>*</b>

A pointer to the Microsoft Active Accessibility object.


### -param idChild [in]

Type: <b>long</b>

The child ID of the Microsoft Active Accessibility object.


### -param dwFlags [in]

Type: <b>DWORD</b>


One of the following values:



<a id="UIA_PFIA_DEFAULT"></a>
<a id="uia_pfia_default"></a>


#### UIA_PFIA_DEFAULT

<a id="UIA_PFIA_UNWRAP_BRIDGE"></a>
<a id="uia_pfia_unwrap_bridge"></a>


#### UIA_PFIA_UNWRAP_BRIDGE


### -param ppProvider [out]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>**</b>

The new UI Automation provider.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



UI Automation provides backward compatibility for Microsoft Active Accessibility providers by supplying a proxy for them, called the Microsoft Active Accessibility to UI Automation proxy.  This proxy is created automatically when a window responds to a <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message by returning a Microsoft Active Accessibility provider.  Use <b>UiaProviderFromIAccessible</b> when you need to create a Microsoft Active Accessibility to UI Automation proxy manually; for example, when implementing the <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> interface.  

Some properties, such as LabeledBy, must be expressed as a UI Automation provider.  An <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> provider can use <b>UiaProviderFromIAccessible</b> to wrap an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> object to return it as the value of the LabeledBy property.





## -see-also




<a href="https://msdn.microsoft.com/76012ec7-0114-4b6b-a35e-5cfde5b90230">Functions for Providers</a>



<a href="https://msdn.microsoft.com/79523637-9858-4E0B-87E7-8CED19FADF0E">UiaIAccessibleFromProvider</a>
 

 

