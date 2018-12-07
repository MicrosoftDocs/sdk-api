---
UID: NF:uiautomationcoreapi.UiaGetPatternProvider
title: UiaGetPatternProvider function
author: windows-sdk-content
description: Retrieves a control pattern.
old-location: winauto\uiauto_UiaGetPatternProviderAutoMeth.htm
tech.root: WinAuto
ms.assetid: f4df6a48-3028-4acb-a924-4c20662a7b86
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UiaGetPatternProvider, UiaGetPatternProvider function [Windows Accessibility], uiauto.uiauto_UiaGetPatternProviderAutoMeth, uiauto_UiaGetPatternProviderAutoMeth, uiautomationcoreapi/UiaGetPatternProvider, winauto.uiauto_UiaGetPatternProviderAutoMeth
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - UiaGetPatternProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaGetPatternProvider function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves a <i>control pattern</i>.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The element that implements the pattern.


### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern being requested. For a list of control pattern IDs, see <a href="https://msdn.microsoft.com/0192e840-96e6-4b12-a570-0d33a36ed885">Control Pattern Identifiers</a>.


### -param phobj [out]

Type: <b>HPATTERNOBJECT*</b>

The address of a variable that receives a handle to the control pattern.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



