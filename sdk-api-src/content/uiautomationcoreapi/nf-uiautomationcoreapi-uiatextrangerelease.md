---
UID: NF:uiautomationcoreapi.UiaTextRangeRelease
title: UiaTextRangeRelease function
author: windows-sdk-content
description: Deletes an allocated text range object from memory.
old-location: winauto\uiauto_UiaTextRangeReleaseMemManMeth.htm
old-project: WinAuto
ms.assetid: 20607071-6300-47f9-8d12-5cf8cc51072a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: UiaTextRangeRelease, UiaTextRangeRelease function [Windows Accessibility], uiauto.uiauto_UiaTextRangeReleaseMemManMeth, uiauto_UiaTextRangeReleaseMemManMeth, uiautomationcoreapi/UiaTextRangeRelease, winauto.uiauto_UiaTextRangeReleaseMemManMeth
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
 - UiaTextRangeRelease
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaTextRangeRelease function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Deletes an allocated text range object from memory.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

The text range object to be deleted.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if object was deleted; otherwise <b>FALSE</b>.



