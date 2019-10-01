---
UID: NF:prsht.PropSheet_IdToIndex
title: PropSheet_IdToIndex macro (prsht.h)
author: windows-sdk-content
description: Takes the resource identifier (ID) of a property sheet page and returns its zero-based index. You can use this macro or send the PSM_IDTOINDEX message explicitly.
old-location: controls\PropSheet_IdToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_idtoindex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropSheet_IdToIndex, PropSheet_IdToIndex macro [Windows Controls], _win32_PropSheet_IdToIndex, _win32_PropSheet_IdToIndex_cpp, controls.PropSheet_IdToIndex, controls._win32_PropSheet_IdToIndex, prsht/PropSheet_IdToIndex
ms.topic: macro
f1_keywords: 
 - "prsht/PropSheet_IdToIndex"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_IdToIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_IdToIndex macro


## -description


Takes the resource identifier (ID) of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/psm-idtoindex">PSM_IDTOINDEX</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet window.


### -param id

Type: <b>int</b>

Resource ID of the page.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propsheet_indextoid">PropSheet_IndexToId</a>
 

 

