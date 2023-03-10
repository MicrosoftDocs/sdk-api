---
UID: NF:shdeprecated.ITravelLog.GetToolTipText
title: ITravelLog::GetToolTipText (shdeprecated.h)
description: Deprecated. Gets tooltip text for a travel entry, which is used as a Unicode display string in the UI.
helpviewer_keywords: ["GetToolTipText","GetToolTipText method [Windows Shell]","GetToolTipText method [Windows Shell]","ITravelLog interface","ITravelLog interface [Windows Shell]","GetToolTipText method","ITravelLog.GetToolTipText","ITravelLog::GetToolTipText","shdeprecated/ITravelLog::GetToolTipText","shell.ITravelLog_GetToolTipText","zone_ITravelLog_GetToolTipText"]
old-location: shell\ITravelLog_GetToolTipText.htm
tech.root: shell
ms.assetid: a085fe2e-9658-448c-b659-4ef08896ec77
ms.date: 12/05/2018
ms.keywords: GetToolTipText, GetToolTipText method [Windows Shell], GetToolTipText method [Windows Shell],ITravelLog interface, ITravelLog interface [Windows Shell],GetToolTipText method, ITravelLog.GetToolTipText, ITravelLog::GetToolTipText, shdeprecated/ITravelLog::GetToolTipText, shell.ITravelLog_GetToolTipText, zone_ITravelLog_GetToolTipText
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
 - ITravelLog::GetToolTipText
 - shdeprecated/ITravelLog::GetToolTipText
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
 - ITravelLog.GetToolTipText
---

# ITravelLog::GetToolTipText


## -description

Deprecated. Gets tooltip text for a travel entry, which is used as a Unicode display string in the UI.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.

### -param iOffset [in]

Type: <b>int</b>

The number of travel entries forward (a positive value) or backward (a negative value) to move in the travel log to arrive at the travel entry from which text should be retrieved.

### -param idsTemplate [in]

Type: <b>int</b>

Not used.

### -param pwzText [out]

Type: <b>LPWSTR</b>

A pointer to a buffer that receives the Unicode tooltip text string.

### -param cchText [in]

Type: <b>DWORD</b>

The number of characters in the buffer pointed to by <i>pwzText</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.