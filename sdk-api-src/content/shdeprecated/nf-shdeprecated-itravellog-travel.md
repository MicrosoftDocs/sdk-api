---
UID: NF:shdeprecated.ITravelLog.Travel
title: ITravelLog::Travel (shdeprecated.h)
description: Deprecated. Navigates to a travel entry in the travel log relative to the position of the current entry.
helpviewer_keywords: ["ITravelLog interface [Windows Shell]","Travel method","ITravelLog.Travel","ITravelLog::Travel","Travel","Travel method [Windows Shell]","Travel method [Windows Shell]","ITravelLog interface","shdeprecated/ITravelLog::Travel","shell.ITravelLog_Travel","zone_ITravelLog_Travel"]
old-location: shell\ITravelLog_Travel.htm
tech.root: shell
ms.assetid: eabe809a-dc02-40fc-9847-88df4cb53e44
ms.date: 12/05/2018
ms.keywords: ITravelLog interface [Windows Shell],Travel method, ITravelLog.Travel, ITravelLog::Travel, Travel, Travel method [Windows Shell], Travel method [Windows Shell],ITravelLog interface, shdeprecated/ITravelLog::Travel, shell.ITravelLog_Travel, zone_ITravelLog_Travel
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
 - ITravelLog::Travel
 - shdeprecated/ITravelLog::Travel
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
 - ITravelLog.Travel
---

# ITravelLog::Travel


## -description

Deprecated. Navigates to a travel entry in the travel log relative to the position of the current entry.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> that represents the nearest browser or frame within which the travel generating the log is taking place.

### -param iOffset [in]

Type: <b>int</b>

The number of travel entries forward (a positive value) or backward (a negative value) to move in the travel log.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling <b>ITravelLog::Travel</b> has the same result as calling <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-itravelentry-invoke">Invoke</a>.