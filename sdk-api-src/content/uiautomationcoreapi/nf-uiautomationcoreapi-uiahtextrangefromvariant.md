---
UID: NF:uiautomationcoreapi.UiaHTextRangeFromVariant
title: UiaHTextRangeFromVariant function
author: windows-sdk-content
description: Gets a text range from a VARIANT type.
old-location: winauto\uiauto_UiaHTextRangeFromVariantFunction.htm
old-project: WinAuto
ms.assetid: 139b970f-614c-42ff-b1d1-4d8644d98d06
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: UiaHTextRangeFromVariant, UiaHTextRangeFromVariant function [Windows Accessibility], uiauto.uiauto_UiaHTextRangeFromVariantFunction, uiauto_UiaHTextRangeFromVariantFunction, uiautomationcoreapi/UiaHTextRangeFromVariant, winauto.uiauto_UiaHTextRangeFromVariantFunction
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
api_name:
-	UiaHTextRangeFromVariant
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaHTextRangeFromVariant function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets a text range from a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> type.


## -parameters




### -param pvar

TBD


### -param phtextrange [out]

Type: <b>HUIATEXTRANGE*</b>

The address of a variable that receives the text range.
				This parameter is passed uninitialized.


#### - par [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>*</b>

The text range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



