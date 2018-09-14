---
UID: NF:uiautomationcoreapi.LegacyIAccessiblePattern_SetValue
title: LegacyIAccessiblePattern_SetValue function
author: windows-sdk-content
description: Sets the Microsoft Active Accessibility value property for the node.
old-location: winauto\uiauto_LegacyIAccessiblePattern_SetValue.htm
tech.root: WinAuto
ms.assetid: ce3fc72b-ddef-4add-a9ff-42763af7ec48
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: LegacyIAccessiblePattern_SetValue, LegacyIAccessiblePattern_SetValue function [Windows Accessibility], uiauto.uiauto_LegacyIAccessiblePattern_SetValue, uiauto_LegacyIAccessiblePattern_SetValue, uiautomationcoreapi/LegacyIAccessiblePattern_SetValue, winauto.uiauto_LegacyIAccessiblePattern_SetValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - LegacyIAccessiblePattern_SetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LegacyIAccessiblePattern_SetValue function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sets the Microsoft Active Accessibility value property for the node.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.


### -param szValue [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A localized string that contains the value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



