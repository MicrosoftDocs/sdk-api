---
UID: NF:ole2.RevokeDragDrop
title: RevokeDragDrop function (ole2.h)
description: Revokes the registration of the specified application window as a potential target for OLE drag-and-drop operations.
helpviewer_keywords: ["RevokeDragDrop","RevokeDragDrop function [COM]","_ole_RevokeDragDrop","com.revokedragdrop","ole2/RevokeDragDrop"]
old-location: com\revokedragdrop.htm
tech.root: com
ms.assetid: c0fa963c-ed06-426c-8ffc-31b02f083a23
ms.date: 12/05/2018
ms.keywords: RevokeDragDrop, RevokeDragDrop function [COM], _ole_RevokeDragDrop, com.revokedragdrop, ole2/RevokeDragDrop
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
 - RevokeDragDrop
 - ole2/RevokeDragDrop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ole32-dragdrop-l1-1-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - RevokeDragDrop
---

# RevokeDragDrop function


## -description

Revokes the registration of the specified application window as a potential target for OLE drag-and-drop operations.

## -parameters

### -param hwnd [in]

Handle to a window previously registered as a target for an OLE drag-and-drop operation.

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
<dt><b>DRAGDROP_E_NOTREGISTERED</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to revoke a drop target that has not been registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_E_INVALIDHWND</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle returned in the <i>hwnd</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory for the operation.

</td>
</tr>
</table>

## -remarks

When your application window is no longer available as a potential target for an OLE drag-and-drop operation, you must call <b>RevokeDragDrop</b>.

This function calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for your drop target interface.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>