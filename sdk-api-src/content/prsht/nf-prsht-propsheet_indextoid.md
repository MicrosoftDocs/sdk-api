---
UID: NF:prsht.PropSheet_IndexToId
title: PropSheet_IndexToId macro
author: windows-sdk-content
description: Takes the index of a property sheet page and returns its resource identifier (ID). You can use this macro or send the PSM_INDEXTOID message explicitly.
old-location: controls\PropSheet_IndexToId.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_indextoid.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PropSheet_IndexToId, PropSheet_IndexToId macro [Windows Controls], _win32_PropSheet_IndexToId, _win32_PropSheet_IndexToId_cpp, controls.PropSheet_IndexToId, controls._win32_PropSheet_IndexToId, prsht/PropSheet_IndexToId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - PropSheet_IndexToId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- prsht.h
: 
- PropSheet_IndexToId
: 
---

# PropSheet_IndexToId macro


## -description


Takes the index of a property sheet page and returns its resource identifier (ID). You can use this macro or send the <a href="https://msdn.microsoft.com/c153675a-360f-4916-aa0b-500636dd9022">PSM_INDEXTOID</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param i

Type: <b>int</b>

Zero-based index of the page.


## -see-also




<a href="https://msdn.microsoft.com/c153675a-360f-4916-aa0b-500636dd9022">PSM_INDEXTOID</a>
 

 

