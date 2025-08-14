---
UID: NF:ole2.OleIsCurrentClipboard
title: OleIsCurrentClipboard function (ole2.h)
description: Determines whether the data object pointer previously placed on the clipboard by the OleSetClipboard function is still on the clipboard.
helpviewer_keywords: ["OleIsCurrentClipboard","OleIsCurrentClipboard function [COM]","_ole_OleIsCurrentClipboard","com.oleiscurrentclipboard","ole2/OleIsCurrentClipboard"]
old-location: com\oleiscurrentclipboard.htm
tech.root: com
ms.assetid: 12844504-ef47-4a4d-b31b-f765e0f2ace6
ms.date: 12/05/2018
ms.keywords: OleIsCurrentClipboard, OleIsCurrentClipboard function [COM], _ole_OleIsCurrentClipboard, com.oleiscurrentclipboard, ole2/OleIsCurrentClipboard
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleIsCurrentClipboard
 - ole2/OleIsCurrentClipboard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
 - API-MS-Win-RTCore-OLE32-clipboard-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-ole32-clipboard-ie-l1-1-0.dll
 - API-MS-Win-RTCore-Ole32-Clipboard-L1-1-1.dll
api_name:
 - OleIsCurrentClipboard
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# OleIsCurrentClipboard function


## -description

Determines whether the data object pointer previously placed on the clipboard by the <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> function is still on the clipboard.

## -parameters

### -param pDataObj [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object containing clipboard data of interest, which the caller previously placed on the clipboard.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer is not on the clipboard.


</td>
</tr>
</table>

## -remarks

<b>OleIsCurrentClipboard</b> only works for the data object used in the <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> function. It cannot be called by the consumer of the data object to determine if the object that was on the clipboard at the previous <a href="/windows/desktop/api/ole2/nf-ole2-olegetclipboard">OleGetClipboard</a> call is still on the clipboard.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a>
