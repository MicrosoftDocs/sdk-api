---
UID: NF:uiautomationcoreapi.TextRange_Clone
title: TextRange_Clone function
author: windows-sdk-content
description: Copies a text range.
old-location: winauto\uiauto_TextRange_CloneConPat.htm
tech.root: WinAuto
ms.assetid: df067f6b-f15f-48cf-979a-d1a9bfbdc05f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: TextRange_Clone, TextRange_Clone function [Windows Accessibility], uiauto.uiauto_TextRange_CloneConPat, uiauto_TextRange_CloneConPat, uiautomationcoreapi/TextRange_Clone, winauto.uiauto_TextRange_CloneConPat
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
 - TextRange_Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TextRange_Clone function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Copies a text range.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.


### -param pRetVal [out]

Type: <b>HUIATEXTRANGE*</b>

When this function returns, contains the copy. 
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



The method never returns <b>NULL</b> (Nothing in Microsoft Visual Basic .NET).

The new range can be manipulated independently from the original.




