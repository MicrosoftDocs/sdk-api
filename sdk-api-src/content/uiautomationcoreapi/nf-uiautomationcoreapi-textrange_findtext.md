---
UID: NF:uiautomationcoreapi.TextRange_FindText
title: TextRange_FindText function
author: windows-sdk-content
description: Returns the first text range in the specified direction that contains the text the client is searching for.
old-location: winauto\uiauto_TextRange_FindTextConPat.htm
tech.root: WinAuto
ms.assetid: 24303a97-e8ad-4261-bff8-575980cf3c3d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: TextRange_FindText, TextRange_FindText function [Windows Accessibility], uiauto.uiauto_TextRange_FindTextConPat, uiauto_TextRange_FindTextConPat, uiautomationcoreapi/TextRange_FindText, winauto.uiauto_TextRange_FindTextConPat
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
 - TextRange_FindText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TextRange_FindText function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Returns the first text range in the specified direction that contains the text the client is searching for.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

The text range to search.


### -param text [in]

Type: <b>BSTR</b>

The string to search for.


### -param backward [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to search backward; otherwise <b>FALSE</b>.


### -param ignoreCase [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to specify a case-insensitive search; otherwise <b>FALSE</b>.


### -param pRetVal [out]

Type: <b>HUITEXTRANGE*</b>

When this function returns, contains 
				the text range for the first span of text that matches the string 
				the client is searching for.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



