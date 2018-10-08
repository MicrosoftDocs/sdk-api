---
UID: NF:uiautomationcoreapi.TextRange_FindAttribute
title: TextRange_FindAttribute function
author: windows-sdk-content
description: Searches in a specified direction for the first piece of text supporting a specified text attribute.
old-location: winauto\uiauto_TextRange_FindAttributeConPat.htm
tech.root: WinAuto
ms.assetid: b5fac0d6-77d7-4fbf-a1b0-4ae0effbd23a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: TextRange_FindAttribute, TextRange_FindAttribute function [Windows Accessibility], uiauto.uiauto_TextRange_FindAttributeConPat, uiauto_TextRange_FindAttributeConPat, uiautomationcoreapi/TextRange_FindAttribute, winauto.uiauto_TextRange_FindAttributeConPat
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
 - TextRange_FindAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TextRange_FindAttribute function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Searches in a specified direction for the first piece of text supporting a specified text attribute.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

The text range to search.


### -param attributeId [in]

Type: <b>TEXTATTRIBUTEID</b>

The text attribute to search for. For a list of text attribute IDs, see <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>.


### -param val [in]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a></b>

The value of the attribute that the client wants to find.


### -param backward [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to search backward, otherwise <b>FALSE</b>.


### -param pRetVal [out]

Type: <b>HUITEXTRANGE*</b>

When this function returns, contains 
				the first matching text range.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



