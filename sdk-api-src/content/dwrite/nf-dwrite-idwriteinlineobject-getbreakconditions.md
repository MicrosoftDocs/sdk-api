---
UID: NF:dwrite.IDWriteInlineObject.GetBreakConditions
title: IDWriteInlineObject::GetBreakConditions
author: windows-sdk-content
description: Layout uses this to determine the line-breaking behavior of the inline object among the text.
old-location: directwrite\IDWriteInlineObject_GetBreakConditions.htm
tech.root: DirectWrite
ms.assetid: c46614a6-2b48-46db-a1e2-73383d6386c5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetBreakConditions, GetBreakConditions method [Direct Write], GetBreakConditions method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],GetBreakConditions method, IDWriteInlineObject.GetBreakConditions, IDWriteInlineObject::GetBreakConditions, directwrite.IDWriteInlineObject_GetBreakConditions, dwrite/IDWriteInlineObject::GetBreakConditions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteInlineObject.GetBreakConditions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteInlineObject.GetBreakConditions
: 
---

# IDWriteInlineObject::GetBreakConditions


## -description


 Layout uses this to determine the line-breaking behavior of the inline object
     among the text.


## -parameters




### -param breakConditionBefore [out]

Type: <b><a href="https://msdn.microsoft.com/26dbe63e-eeee-486f-aa94-74320b190fcb">DWRITE_BREAK_CONDITION</a>*</b>

When this method returns, contains a value which indicates the line-breaking condition between the object and the content immediately preceding it.


### -param breakConditionAfter [out]

Type: <b><a href="https://msdn.microsoft.com/26dbe63e-eeee-486f-aa94-74320b190fcb">DWRITE_BREAK_CONDITION</a>*</b>

When this method returns, contains a value which indicates the line-breaking condition between the object and the content immediately following it.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>
 

 

