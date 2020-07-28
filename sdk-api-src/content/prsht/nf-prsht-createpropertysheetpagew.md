---
UID: NF:prsht.CreatePropertySheetPageW
title: CreatePropertySheetPageW function (prsht.h)
description: Creates a new page for a property sheet.
helpviewer_keywords: ["CreatePropertySheetPage","CreatePropertySheetPage function [Windows Controls]","CreatePropertySheetPageA","CreatePropertySheetPageW","_win32_CreatePropertySheetPage","_win32_CreatePropertySheetPage_cpp","controls.CreatePropertySheetPage","controls._win32_CreatePropertySheetPage","prsht/CreatePropertySheetPage","prsht/CreatePropertySheetPageA","prsht/CreatePropertySheetPageW"]
old-location: controls\CreatePropertySheetPage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\createpropertysheetpage.htm
ms.date: 12/05/2018
ms.keywords: CreatePropertySheetPage, CreatePropertySheetPage function [Windows Controls], CreatePropertySheetPageA, CreatePropertySheetPageW, _win32_CreatePropertySheetPage, _win32_CreatePropertySheetPage_cpp, controls.CreatePropertySheetPage, controls._win32_CreatePropertySheetPage, prsht/CreatePropertySheetPage, prsht/CreatePropertySheetPageA, prsht/CreatePropertySheetPageW
f1_keywords:
- prsht/CreatePropertySheetPage
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreatePropertySheetPageW function


## -description


Creates a new page for a property sheet.


## -parameters




### -param constPropSheetPagePointer

Type: <b>LPCPROPSHEETPAGE</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure that defines a page to be included in a property sheet.


## -returns



Type: <b>HPROPSHEETPAGE</b>

Returns the handle to the new property page if successful, or <b>NULL</b> otherwise.




## -remarks



<div class="alert"><b>Note</b>  Before common controls version 7.0, this function did not support visual styles.</div>
<div> </div>
An application uses the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function to create a property sheet that includes the new page. If you are not using the Aero wizard style (<a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>), the application can use the <a href="https://docs.microsoft.com/windows/desktop/Controls/psm-addpage">PSM_ADDPAGE</a> message to add the new page to an existing property sheet.

Windows 95: The system can support a maximum of 16,364 window handles.




> [!NOTE]
> The prsht.h header defines CreatePropertySheetPage as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

