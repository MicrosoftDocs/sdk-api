---
UID: NF:shdeprecated.ITravelLog.UpdateEntry
title: ITravelLog::UpdateEntry (shdeprecated.h)
description: Deprecated. Saves the browser state of the current entry in preparation for a pending navigation.
helpviewer_keywords: ["FALSE","ITravelLog interface [Windows Shell]","UpdateEntry method","ITravelLog.UpdateEntry","ITravelLog::UpdateEntry","TRUE","UpdateEntry","UpdateEntry method [Windows Shell]","UpdateEntry method [Windows Shell]","ITravelLog interface","shdeprecated/ITravelLog::UpdateEntry","shell.ITravelLog_UpdateEntry","zone_ITravelLog_UpdateEntry"]
old-location: shell\ITravelLog_UpdateEntry.htm
tech.root: shell
ms.assetid: 63fe398d-c0e8-4350-9b57-fe9f11e24e47
ms.date: 12/05/2018
ms.keywords: FALSE, ITravelLog interface [Windows Shell],UpdateEntry method, ITravelLog.UpdateEntry, ITravelLog::UpdateEntry, TRUE, UpdateEntry, UpdateEntry method [Windows Shell], UpdateEntry method [Windows Shell],ITravelLog interface, shdeprecated/ITravelLog::UpdateEntry, shell.ITravelLog_UpdateEntry, zone_ITravelLog_UpdateEntry
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
 - ITravelLog::UpdateEntry
 - shdeprecated/ITravelLog::UpdateEntry
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
 - ITravelLog.UpdateEntry
---

# ITravelLog::UpdateEntry


## -description

Deprecated. Saves the browser state of the current entry in preparation for a pending navigation.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> that represents the nearest browser or frame within which the travel generating the log is taking place.

### -param fIsLocalAnchor [in]

Type: <b>BOOL</b>

A value specifying whether the new entry is a local anchor.



#### TRUE

The entry is an anchor link within the same page.



#### FALSE

The entry is another page or an anchor on another page.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.