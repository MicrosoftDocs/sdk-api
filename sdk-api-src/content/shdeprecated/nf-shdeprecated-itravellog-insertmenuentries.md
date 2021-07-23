---
UID: NF:shdeprecated.ITravelLog.InsertMenuEntries
title: ITravelLog::InsertMenuEntries (shdeprecated.h)
description: Deprecated. Inserts entries into the specified menu.
helpviewer_keywords: ["ITravelLog interface [Windows Shell]","InsertMenuEntries method","ITravelLog.InsertMenuEntries","ITravelLog::InsertMenuEntries","InsertMenuEntries","InsertMenuEntries method [Windows Shell]","InsertMenuEntries method [Windows Shell]","ITravelLog interface","TLMENUF_BACK","TLMENUF_BACKANDFORTH","TLMENUF_CHECKCURRENT","TLMENUF_FORE","TLMENUF_INCLUDECURRENT","shdeprecated/ITravelLog::InsertMenuEntries","shell.ITravelLog_InsertMenuEntries","zone_ITravelLog_InsertMenuEntries"]
old-location: shell\ITravelLog_InsertMenuEntries.htm
tech.root: shell
ms.assetid: 5e75c524-5fa6-4d76-8fe9-a69ee1b509e8
ms.date: 12/05/2018
ms.keywords: ITravelLog interface [Windows Shell],InsertMenuEntries method, ITravelLog.InsertMenuEntries, ITravelLog::InsertMenuEntries, InsertMenuEntries, InsertMenuEntries method [Windows Shell], InsertMenuEntries method [Windows Shell],ITravelLog interface, TLMENUF_BACK, TLMENUF_BACKANDFORTH, TLMENUF_CHECKCURRENT, TLMENUF_FORE, TLMENUF_INCLUDECURRENT, shdeprecated/ITravelLog::InsertMenuEntries, shell.ITravelLog_InsertMenuEntries, zone_ITravelLog_InsertMenuEntries
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - ITravelLog::InsertMenuEntries
 - shdeprecated/ITravelLog::InsertMenuEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITravelLog.InsertMenuEntries
---

# ITravelLog::InsertMenuEntries


## -description

Deprecated. Inserts entries into the specified menu.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.

### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the menu.

### -param nPos [in]

Type: <b>int</b>

The position in the menu to insert the entries.

### -param idFirst [in]

Type: <b>int</b>

The ID of the first entry to be inserted.

### -param idLast [in]

Type: <b>int</b>

The ID of the last entry to be inserted. The difference between <i>idFirst</i> and <i>idLast</i> is the maximum number of entries that can be inserted into the menu.

### -param dwFlags [in]

Type: <b>DWORD</b>

The types of entries to add to the menu. Includes the following:



#### TLMENUF_INCLUDECURRENT

Include the current page.



#### TLMENUF_CHECKCURRENT

Add a check mark next to the entry of the current page.



#### TLMENUF_BACK

Default. The previous pages.



#### TLMENUF_FORE

The next pages.



#### TLMENUF_BACKANDFORTH

Previous, current, and next pages.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.