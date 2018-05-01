---
UID: NF:prsht.CreatePropertySheetPageW
title: CreatePropertySheetPageW function
author: windows-driver-content
description: Creates a new page for a property sheet.
old-location: controls\CreatePropertySheetPage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\createpropertysheetpage.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	CreatePropertySheetPage
-	CreatePropertySheetPageA
-	CreatePropertySheetPageW
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CreatePropertySheetPageW function


## -description


Creates a new page for a property sheet.


## -parameters




### -param constPropSheetPagePointer

TBD




#### - lppsp

Type: <b>LPCPROPSHEETPAGE</b>

Pointer to a <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> structure that defines a page to be included in a property sheet.


## -returns



Type: <b>HPROPSHEETPAGE</b>

Returns the handle to the new property page if successful, or <b>NULL</b> otherwise.




## -remarks



<div class="alert"><b>Note</b>  Before common controls version 7.0, this function did not support visual styles.</div>
<div> </div>
An application uses the <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function to create a property sheet that includes the new page. If you are not using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>), the application can use the <a href="https://msdn.microsoft.com/41f9a09e-6de6-466b-bdfa-c8c4e8f193e4">PSM_ADDPAGE</a> message to add the new page to an existing property sheet.

Windows 95: The system can support a maximum of 16,364 window handles.



