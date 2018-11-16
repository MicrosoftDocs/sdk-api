---
UID: NF:prsht.CreatePropertySheetPageA
title: CreatePropertySheetPageA function
author: windows-sdk-content
description: Creates a new page for a property sheet.
old-location: controls\CreatePropertySheetPage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\createpropertysheetpage.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreatePropertySheetPage, CreatePropertySheetPage function [Windows Controls], CreatePropertySheetPageA, CreatePropertySheetPageW, _win32_CreatePropertySheetPage, _win32_CreatePropertySheetPage_cpp, controls.CreatePropertySheetPage, controls._win32_CreatePropertySheetPage, prsht/CreatePropertySheetPage, prsht/CreatePropertySheetPageA, prsht/CreatePropertySheetPageW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreatePropertySheetPageW (Unicode) and CreatePropertySheetPageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - CreatePropertySheetPage
 - CreatePropertySheetPageA
 - CreatePropertySheetPageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreatePropertySheetPageA
: 
---

# CreatePropertySheetPageA function


## -description


Creates a new page for a property sheet.


## -parameters




### -param constPropSheetPagePointer

Type: <b>LPCPROPSHEETPAGE</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb774548(v=VS.85).aspx">PROPSHEETPAGE</a> structure that defines a page to be included in a property sheet.


## -returns



Type: <b>HPROPSHEETPAGE</b>

Returns the handle to the new property page if successful, or <b>NULL</b> otherwise.




## -remarks



<div class="alert"><b>Note</b>  Before common controls version 7.0, this function did not support visual styles.</div>
<div> </div>
An application uses the <a href="https://msdn.microsoft.com/en-us/library/Bb760811(v=VS.85).aspx">PropertySheet</a> function to create a property sheet that includes the new page. If you are not using the Aero wizard style (<a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>), the application can use the <a href="https://msdn.microsoft.com/en-us/library/Bb774573(v=VS.85).aspx">PSM_ADDPAGE</a> message to add the new page to an existing property sheet.

Windows 95: The system can support a maximum of 16,364 window handles.



