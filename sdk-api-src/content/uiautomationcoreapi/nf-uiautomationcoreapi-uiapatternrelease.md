---
UID: NF:uiautomationcoreapi.UiaPatternRelease
title: UiaPatternRelease function
author: windows-sdk-content
description: Deletes an allocated pattern object from memory.
old-location: winauto\uiauto_UiaPatternReleaseMemManMeth.htm
old-project: WinAuto
ms.assetid: caa7231b-5b31-499e-b548-479501ddf016
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: UiaPatternRelease, UiaPatternRelease function [Windows Accessibility], uiauto.uiauto_UiaPatternReleaseMemManMeth, uiauto_UiaPatternReleaseMemManMeth, uiautomationcoreapi/UiaPatternRelease, winauto.uiauto_UiaPatternReleaseMemManMeth
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
-	UiaPatternRelease
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaPatternRelease function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Deletes an allocated pattern object from memory.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The pattern object to be deleted.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the pattern was successfully deleted; otherwise <b>FALSE</b>.



