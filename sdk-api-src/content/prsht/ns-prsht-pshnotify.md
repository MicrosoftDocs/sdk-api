---
UID: NS:prsht._PSHNOTIFY
title: PSHNOTIFY (prsht.h)
description: Contains information for the property sheet notification messages.
helpviewer_keywords: ["*LPPSHNOTIFY","LPPSHNOTIFY","LPPSHNOTIFY structure pointer [Windows Controls]","PSHNOTIFY","PSHNOTIFY structure [Windows Controls]","_win32_PSHNOTIFY","_win32_PSHNOTIFY_cpp","controls.PSHNOTIFY","controls._win32_PSHNOTIFY","prsht/LPPSHNOTIFY","prsht/PSHNOTIFY"]
old-location: controls\PSHNOTIFY.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\structures\pshnotify.htm
ms.date: 12/05/2018
ms.keywords: '*LPPSHNOTIFY, LPPSHNOTIFY, LPPSHNOTIFY structure pointer [Windows Controls], PSHNOTIFY, PSHNOTIFY structure [Windows Controls], _win32_PSHNOTIFY, _win32_PSHNOTIFY_cpp, controls.PSHNOTIFY, controls._win32_PSHNOTIFY, prsht/LPPSHNOTIFY, prsht/PSHNOTIFY'
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
targetos: Windows
req.typenames: PSHNOTIFY, *LPPSHNOTIFY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSHNOTIFY
 - prsht/_PSHNOTIFY
 - LPPSHNOTIFY
 - prsht/LPPSHNOTIFY
 - PSHNOTIFY
 - prsht/PSHNOTIFY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PSHNOTIFY
---

# PSHNOTIFY structure


## -description

Contains information for the property sheet notification messages.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

Address of an <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Additional information about this notification. To determine what, if any, information is contained in this member, see the description of the particular notification message.