---
UID: NF:uiautomationcoreapi.TextRange_GetAttributeValue
title: TextRange_GetAttributeValue function
author: windows-sdk-content
description: Gets the value of an text attribute for a text range.
old-location: winauto\uiauto_TextRange_GetAttributeValueConPat.htm
tech.root: WinAuto
ms.assetid: f5d90dba-7c84-45a8-be84-898d6079c428
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: TextRange_GetAttributeValue, TextRange_GetAttributeValue function [Windows Accessibility], uiauto.uiauto_TextRange_GetAttributeValueConPat, uiauto_TextRange_GetAttributeValueConPat, uiautomationcoreapi/TextRange_GetAttributeValue, winauto.uiauto_TextRange_GetAttributeValueConPat
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
 - TextRange_GetAttributeValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TextRange_GetAttributeValue function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the value of an text attribute for a text range.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.


### -param attributeId [in]

Type: <b>TEXTATTRIBUTEID</b>

The text attribute whose value is wanted. For a list of text attribute IDs, see <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>.


### -param pRetVal [out]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a>*</b>

When this function returns, contains 
				the value of the attribute for the text range.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



