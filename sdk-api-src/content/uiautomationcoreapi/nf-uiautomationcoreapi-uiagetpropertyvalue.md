---
UID: NF:uiautomationcoreapi.UiaGetPropertyValue
title: UiaGetPropertyValue function
author: windows-sdk-content
description: Retrieves the value of a UI Automation property.
old-location: winauto\uiauto_UiaGetPropertyValueAutoMeth.htm
old-project: WinAuto
ms.assetid: 17d5450c-0894-412f-a8d1-44ea0364a606
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: UiaGetPropertyValue, UiaGetPropertyValue function [Windows Accessibility], uiauto.uiauto_UiaGetPropertyValueAutoMeth, uiauto_UiaGetPropertyValueAutoMeth, uiautomationcoreapi/UiaGetPropertyValue, winauto.uiauto_UiaGetPropertyValueAutoMeth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaGetPropertyValue
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaGetPropertyValue function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the value of a UI Automation property.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The element that the property is being requested from.


### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param pValue

TBD




#### - pvalue [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>*</b>

Receives the value of the specified property, or the value returned by <a href="https://msdn.microsoft.com/ba789ed0-fa34-492c-90b4-acee0adb634c">UiaGetReservedNotSupportedValue</a> if the property is not supported.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



