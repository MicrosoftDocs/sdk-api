---
UID: NF:uiautomationcoreapi.SelectionItemPattern_RemoveFromSelection
title: SelectionItemPattern_RemoveFromSelection function
author: windows-sdk-content
description: Removes an element from the selection in a selection container.
old-location: winauto\uiauto_SelectionItemPattern_RemoveFromSelectionConPat.htm
tech.root: WinAuto
ms.assetid: 190e02a5-1ea9-44cc-a215-cabc700ec814
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SelectionItemPattern_RemoveFromSelection, SelectionItemPattern_RemoveFromSelection function [Windows Accessibility], uiauto.uiauto_SelectionItemPattern_RemoveFromSelectionConPat, uiauto_SelectionItemPattern_RemoveFromSelectionConPat, uiautomationcoreapi/SelectionItemPattern_RemoveFromSelection, winauto.uiauto_SelectionItemPattern_RemoveFromSelectionConPat
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
 - SelectionItemPattern_RemoveFromSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SelectionItemPattern_RemoveFromSelection function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Removes an element from the selection in a selection container.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



The function has no effect if an attempt is made to remove the last selected element in a control that requires at
least one element to be selected.



