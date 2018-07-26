---
UID: NF:ole2.OleSetClipboard
title: OleSetClipboard function
author: windows-sdk-content
description: Places a pointer to a specific data object onto the clipboard. This makes the data object accessible to the OleGetClipboard function.
old-location: com\olesetclipboard.htm
old-project: com
ms.assetid: 741def10-d2b5-4395-8049-1eba2e29b0e8
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OleSetClipboard, OleSetClipboard function [COM], _ole_OleSetClipboard, com.olesetclipboard, ole2/OleSetClipboard
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-RTCore-OLE32-clipboard-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-ole32-clipboard-ie-l1-1-0.dll
 - API-MS-Win-RTCore-Ole32-Clipboard-L1-1-1.dll
api_name:
 - OleSetClipboard
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleSetClipboard function


## -description


Places a pointer to a specific data object onto the clipboard. This makes the data object accessible to the <a href="https://msdn.microsoft.com/c5e7badb-339b-48d5-8c9a-3950e2ffe6bf">OleGetClipboard</a> function.




## -parameters




### -param pDataObj [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object from which the data to be placed on the clipboard can be obtained. This parameter can be <b>NULL</b>; in which case the clipboard is emptied.


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
<dt><b>CLIPBRD_E_CANT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/library/ms649048(v=VS.85).aspx">OpenClipboard</a> function used within <a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a> failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLIPBRD_E_CANT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/library/ms649037(v=VS.85).aspx">EmptyClipboard</a> function used within <a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a> failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLIPBRD_E_CANT_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/library/ms649035(v=VS.85).aspx">CloseClipboard</a> function used within <a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a> failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLIPBRD_E_CANT_SET</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/library/ms649051(v=VS.85).aspx">SetClipboardData</a> function used within <a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a> failed.

</td>
</tr>
</table>
 




## -remarks



If you are writing an application that can act as the source of a clipboard operation, you must do the following:

<ul>
<li>Create a data object (on which is the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface) for the data being copied or cut to the clipboard. This object should be the same object used in OLE drag-and-drop operations.</li>
<li>Call <b>OleSetClipboard</b> to place the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> pointer onto the clipboard, so it is accessible to the <a href="https://msdn.microsoft.com/c5e7badb-339b-48d5-8c9a-3950e2ffe6bf">OleGetClipboard</a> function. <b>OleSetClipboard</b> also calls the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> method on your data object.</li>
<li>If you wish, release the data object after you have placed it on the clipboard to free the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> counter in your application.</li>
<li>If the user is cutting data (deleting it from the document and putting it on to the clipboard), remove the data from the document.</li>
</ul>
All formats are offered on the clipboard using delayed rendering (the clipboard contains only a pointer to the data object unless a call to <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a> renders the data onto the clipboard). The formats necessary for OLE 1 compatibility are synthesized from the OLE 2 formats that are present and are also put on the clipboard.

The <b>OleSetClipboard</b> function assigns ownership of the clipboard to an internal OLE window handle. The reference count of the data object is increased by 1, to enable delayed rendering. The reference count is decreased by a call to the <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a> function or by a subsequent call to <b>OleSetClipboard</b> specifying <b>NULL</b> as the parameter value (which clears the clipboard).



When an application opens the clipboard (either directly or indirectly by calling the <a href="https://msdn.microsoft.com/library/ms649048(v=VS.85).aspx">OpenClipboard</a> function), the clipboard cannot be used by any other application until it is closed. If the clipboard is currently open by another application, <b>OleSetClipboard</b> fails. The internal OLE window handle satisfies WM_RENDERFORMAT messages by delegating them to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> implementation on the data object that is on the clipboard.

Specifying <b>NULL</b> as the parameter value for <b>OleSetClipboard</b> empties the current clipboard. If the contents of the clipboard are the result of a previous <b>OleSetClipboard</b> call and the clipboard has been released, the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> pointer that was passed to the previous call is released. The clipboard owner should use this as a signal that the data it previously offered is no longer on the clipboard.



If you need to leave the data on the clipboard after your application is closed, you should call <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a> rather than calling <b>OleSetClipboard</b> with a <b>NULL</b> parameter value.

If you need to leave the data on the clipboard after your application is closed, you should call <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a> rather than calling <b>OleSetClipboard</b> with a <b>NULL</b> parameter value.




## -see-also




<a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a>



<a href="https://msdn.microsoft.com/c5e7badb-339b-48d5-8c9a-3950e2ffe6bf">OleGetClipboard</a>



<a href="https://msdn.microsoft.com/12844504-ef47-4a4d-b31b-f765e0f2ace6">OleIsCurrentClipboard</a>
 

 

