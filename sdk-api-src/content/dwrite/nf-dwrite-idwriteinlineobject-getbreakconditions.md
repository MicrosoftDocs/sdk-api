---
UID: NF:dwrite.IDWriteInlineObject.GetBreakConditions
title: IDWriteInlineObject::GetBreakConditions (dwrite.h)
description: Layout uses this to determine the line-breaking behavior of the inline object among the text.
helpviewer_keywords: ["GetBreakConditions","GetBreakConditions method [Direct Write]","GetBreakConditions method [Direct Write]","IDWriteInlineObject interface","IDWriteInlineObject interface [Direct Write]","GetBreakConditions method","IDWriteInlineObject.GetBreakConditions","IDWriteInlineObject::GetBreakConditions","directwrite.IDWriteInlineObject_GetBreakConditions","dwrite/IDWriteInlineObject::GetBreakConditions"]
old-location: directwrite\IDWriteInlineObject_GetBreakConditions.htm
tech.root: DirectWrite
ms.assetid: c46614a6-2b48-46db-a1e2-73383d6386c5
ms.date: 12/05/2018
ms.keywords: GetBreakConditions, GetBreakConditions method [Direct Write], GetBreakConditions method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],GetBreakConditions method, IDWriteInlineObject.GetBreakConditions, IDWriteInlineObject::GetBreakConditions, directwrite.IDWriteInlineObject_GetBreakConditions, dwrite/IDWriteInlineObject::GetBreakConditions
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteInlineObject::GetBreakConditions
 - dwrite/IDWriteInlineObject::GetBreakConditions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteInlineObject.GetBreakConditions
---

# IDWriteInlineObject::GetBreakConditions


## -description

 Layout uses this to determine the line-breaking behavior of the inline object
     among the text.

## -parameters

### -param breakConditionBefore [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition">DWRITE_BREAK_CONDITION</a>*</b>

When this method returns, contains a value which indicates the line-breaking condition between the object and the content immediately preceding it.

### -param breakConditionAfter [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition">DWRITE_BREAK_CONDITION</a>*</b>

When this method returns, contains a value which indicates the line-breaking condition between the object and the content immediately following it.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>

