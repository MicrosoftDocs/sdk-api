---
UID: NF:uiautomationcoreapi.TextRange_GetText
title: TextRange_GetText function
author: windows-sdk-content
description: Returns the text in a text range, up to a specified number of characters.
old-location: winauto\uiauto_TextRange_GetTextConPat.htm
tech.root: WinAuto
ms.assetid: 1c8ba026-0c85-46a0-a667-daba0191b115
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: TextRange_GetText, TextRange_GetText function [Windows Accessibility], uiauto.uiauto_TextRange_GetTextConPat, uiauto_TextRange_GetTextConPat, uiautomationcoreapi/TextRange_GetText, winauto.uiauto_TextRange_GetTextConPat
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
 - TextRange_GetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TextRange_GetText function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Returns the text in a text range, up to a specified number of characters.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.


### -param maxLength [in]

Type: <b>int</b>

The number of characters to return, beginning with the character at the starting endpoint of the text range.


### -param pRetVal [out]

Type: <b>BSTR*</b>

When this function returns, this parameter contains 
				a pointer to the returned text.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



If <i>maxLength</i> is -1, all of the text within the text range is returned. 
If <i>maxLength</i> is larger than the length of the text range, the returned string contains all of the text in the text range.



