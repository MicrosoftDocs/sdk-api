---
UID: NF:prsht.DestroyPropertySheetPage
title: DestroyPropertySheetPage function (prsht.h)

description: Destroys a property sheet page. An application must call this function for pages that have not been passed to the PropertySheet function.
old-location: controls\DestroyPropertySheetPage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\destroypropertysheetpage.htm

ms.date: 12/05/2018
ms.keywords: DestroyPropertySheetPage, DestroyPropertySheetPage function [Windows Controls], _win32_DestroyPropertySheetPage, _win32_DestroyPropertySheetPage_cpp, controls.DestroyPropertySheetPage, controls._win32_DestroyPropertySheetPage, prsht/DestroyPropertySheetPage
ms.topic: function
f1_keywords: 
 - "prsht/DestroyPropertySheetPage"
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
req.unicode-ansi: 
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
 - DestroyPropertySheetPage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DestroyPropertySheetPage function


## -description


Destroys a property sheet page. An application must call this function for pages that have not been passed to the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function.


## -parameters




### -param Arg1

Type: <b>HPROPSHEETPAGE</b>

Handle to the property sheet page to delete.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.



