---
UID: NF:uiautomationcoreapi.UiaHPatternObjectFromVariant
title: UiaHPatternObjectFromVariant function
author: windows-sdk-content
description: Gets a control pattern object from a VARIANT type.
old-location: winauto\uiauto_UiaHPatternObjectFromVariantFunction.htm
tech.root: WinAuto
ms.assetid: dd5d0d4b-75fa-4215-bd48-79d58a9a4862
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: UiaHPatternObjectFromVariant, UiaHPatternObjectFromVariant function [Windows Accessibility], uiauto.uiauto_UiaHPatternObjectFromVariantFunction, uiauto_UiaHPatternObjectFromVariantFunction, uiautomationcoreapi/UiaHPatternObjectFromVariant, winauto.uiauto_UiaHPatternObjectFromVariantFunction
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
 - UiaHPatternObjectFromVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaHPatternObjectFromVariant function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets a control pattern object from a <a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> type.


## -parameters




### -param pvar [in]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a>*</b>

The pattern.


### -param phobj [out]

Type: <b>HUIAPATTERNOBJECT *</b>

The address of a variable that receives the control pattern object.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



