---
UID: NS:shlobj_core._SFVM_PROPPAGE_DATA
title: SFVM_PROPPAGE_DATA (shlobj_core.h)
author: windows-sdk-content
description: Contains the details of a page to be added to an object's Properties sheet.
old-location: shell\SFVM_PROPPAGE_DATA.htm
tech.root: shell
ms.assetid: 9f214786-fc82-4f1b-a0ec-7bf61b1f3cf7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SFVM_PROPPAGE_DATA, SFVM_PROPPAGE_DATA structure [Windows Shell], _SFVM_PROPPAGE_DATA, _win32_SFVM_PROPPAGE_DATA, shell.SFVM_PROPPAGE_DATA, shlobj_core/SFVM_PROPPAGE_DATA
ms.topic: struct
f1_keywords: 
 - "shlobj_core/SFVM_PROPPAGE_DATA"
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SFVM_PROPPAGE_DATA
product: Windows
targetos: Windows
req.typenames: SFVM_PROPPAGE_DATA
req.redist: 
ms.custom: 19H1
---

# SFVM_PROPPAGE_DATA structure


## -description


Contains the details of a page to be added to an object's <b>Properties</b> sheet.


## -struct-fields




### -field dwReserved

Type: <b>DWORD</b>


### -field pfn

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/prsht/nc-prsht-lpfnaddpropsheetpage">AddPropSheetPageProc</a> callback function used to add property pages. When this function is used by Windows Explorer, it provides <b>pfn</b> through the system folder view object's <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages">IShellView::AddPropertySheetPages</a> method. The callback function can then pass the information to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages">IShellPropSheetExt::AddPages</a>.


### -field lParam

Type: <b>LPARAM</b>

The details of the property sheet to be added. When this function is used by Windows Explorer, it provides <b>lParam</b> through the system folder view object's <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages">IShellView::AddPropertySheetPages</a> method. The callback function can then pass the information to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages">IShellPropSheetExt::AddPages</a>.

