---
UID: NS:htmlhelp.tagHHNTRACK
title: HHNTRACK (htmlhelp.h)
description: This structure returns the file name of the current topic and a constant that specifies the user action that is about to occur, such as hiding the Navigation pane by clicking the Hide button on the toolbar.
helpviewer_keywords: ["HHNTRACK","HHNTRACK structure [HTML Help Workshop]","htmlhelp.hhntrack_structure","htmlhelp/HHNTRACK","vsconStrhhntrack"]
old-location: htmlhelp\hhntrack_structure.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhntrack.htm
ms.date: 12/05/2018
ms.keywords: HHNTRACK, HHNTRACK structure [HTML Help Workshop], htmlhelp.hhntrack_structure, htmlhelp/HHNTRACK, vsconStrhhntrack
req.header: htmlhelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: HHNTRACK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHHNTRACK
 - htmlhelp/tagHHNTRACK
 - HHNTRACK
 - htmlhelp/HHNTRACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HtmlHelp.h
api_name:
 - HHNTRACK
---

# HHNTRACK structure


## -description

This structure returns the file name of the current topic and a constant that specifies the user action that is about to occur, such as hiding the Navigation pane by clicking the Hide button on the toolbar.

## -struct-fields

### -field hdr

Standard <b>WM_NOTIFY</b> header.

### -field pszCurUrl

A multi-byte, zero-terminated string that specifies the current topic (before the action is taken).

### -field idAction

Specifies the action the user is about to take. This is an <a href="/previous-versions/windows/desktop/htmlhelp/idaction-member">HHACT_</a> constant.

### -field phhWinType

A pointer to the current <a href="/windows/desktop/api/htmlhelp/ns-htmlhelp-hh_wintype">HH_WINTYPE</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/htmlhelp/about-structures">About structures</a>