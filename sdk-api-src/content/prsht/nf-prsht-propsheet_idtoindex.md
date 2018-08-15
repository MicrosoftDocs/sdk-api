---
UID: NF:prsht.PropSheet_IdToIndex
title: PropSheet_IdToIndex macro
author: windows-sdk-content
description: Takes the resource identifier (ID) of a property sheet page and returns its zero-based index. You can use this macro or send the PSM_IDTOINDEX message explicitly.
old-location: controls\PropSheet_IdToIndex.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_idtoindex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropSheet_IdToIndex, PropSheet_IdToIndex macro [Windows Controls], _win32_PropSheet_IdToIndex, _win32_PropSheet_IdToIndex_cpp, controls.PropSheet_IdToIndex, controls._win32_PropSheet_IdToIndex, prsht/PropSheet_IdToIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: prsht.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_IdToIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_IdToIndex macro


## -description


Takes the resource identifier (ID) of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://msdn.microsoft.com/91420c1e-7f8a-4b1c-a1fc-6ff65ee4b1b0">PSM_IDTOINDEX</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet window.


### -param id

Type: <b>int</b>

Resource ID of the page.


## -see-also




<a href="https://msdn.microsoft.com/358f9904-5b14-42e4-8095-f7b4d8144bc2">PropSheet_IndexToId</a>
 

 

