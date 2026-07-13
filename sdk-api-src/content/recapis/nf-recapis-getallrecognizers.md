---
UID: NF:recapis.GetAllRecognizers
title: GetAllRecognizers function (recapis.h)
description: Gets all recognizers.
helpviewer_keywords: ["GetAllRecognizers","GetAllRecognizers function [Tablet PC]","recapis/GetAllRecognizers","tablet.getallrecognizers"]
old-location: tablet\getallrecognizers.htm
tech.root: tablet
ms.assetid: F2039094-E3B0-4FF4-9B69-ED29D681B388
ms.date: 12/05/2018
ms.keywords: GetAllRecognizers, GetAllRecognizers function [Tablet PC], recapis/GetAllRecognizers, tablet.getallrecognizers
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAllRecognizers
 - recapis/GetAllRecognizers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetAllRecognizers
---

# GetAllRecognizers function


## -description



Gets all recognizers.

## -parameters

### -param recognizerClsids

Pointer to the CLSIDs of the recognizers. The CLSID value is created in the registry when you register the recognizer.

### -param count

Pointer to the number of recognizers.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>

