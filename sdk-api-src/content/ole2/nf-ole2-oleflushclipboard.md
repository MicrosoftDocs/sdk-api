---
UID: NF:ole2.OleFlushClipboard
title: OleFlushClipboard function (ole2.h)
description: Carries out the clipboard shutdown sequence. It also releases the IDataObject pointer that was placed on the clipboard by the OleSetClipboard function.
helpviewer_keywords: ["OleFlushClipboard","OleFlushClipboard function [COM]","_ole_OleFlushClipboard","com.oleflushclipboard","ole2/OleFlushClipboard"]
old-location: com\oleflushclipboard.htm
tech.root: com
ms.assetid: 18291a91-be7d-42ec-a44a-d1bbfb017c6e
ms.date: 12/05/2018
ms.keywords: OleFlushClipboard, OleFlushClipboard function [COM], _ole_OleFlushClipboard, com.oleflushclipboard, ole2/OleFlushClipboard
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
 - OleFlushClipboard
 - ole2/OleFlushClipboard
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
 - OleFlushClipboard
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# OleFlushClipboard function


## -description

Carries out the clipboard shutdown sequence. It also releases the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> pointer that was placed on the clipboard by the <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> function.



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
The Windows OpenClipboard function used within <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLIPBRD_E_CANT_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
The Windows CloseClipboard function used within <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> failed.

</td>
</tr>
</table>

## -remarks

<b>OleFlushClipboard</b> renders the data from a data object onto the clipboard and releases the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> pointer to the data object. While the application that put the data object on the clipboard is running, the clipboard holds only a pointer to the data object, thus saving memory. If you are writing an application that acts as the source of a clipboard operation, you can call the <b>OleFlushClipboard</b> function when your application is closed, such as when the user exits from your application. Calling <b>OleFlushClipboard</b> enables pasting and paste-linking of OLE objects after application shutdown.

Before calling <b>OleFlushClipboard</b>, you can easily determine if your data is still on the clipboard with a call to the <a href="/windows/desktop/api/ole2/nf-ole2-oleiscurrentclipboard">OleIsCurrentClipboard</a> function.

<b>OleFlushClipboard</b> leaves all formats offered by the data transfer object, including the OLE 1 compatibility formats, on the clipboard so they are available after application shutdown. In addition to OLE 1 compatibility formats, these include all formats offered on a global handle medium (all except for TYMED_FILE) and formatted with a <b>NULL</b> target device. For example, if a data-source application offers a particular clipboard format (say cfFOO) on an <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> object, and calls the <b>OleFlushClipboard</b> function, the storage object is copied into memory and the hglobal memory handle is put on the clipboard.

To retrieve the information on the clipboard, you can call the <a href="/windows/desktop/api/ole2/nf-ole2-olegetclipboard">OleGetClipboard</a> function from another application, which creates a default data object, and the hglobal from the clipboard again becomes a storage object. Furthermore, the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> enumerator and the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-querygetdata">IDataObject::QueryGetData</a> method would all correctly indicate that the original clipboard format (cfFOO) is again available on a TYMED_ISTORAGE.

To empty the clipboard, call the <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> function specifying a <b>NULL</b> value for its parameter. The application should call this when it closes if there is no need to leave data on the clipboard after shutdown, or if data will be placed on the clipboard using the standard Windows clipboard functions.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olegetclipboard">OleGetClipboard</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleiscurrentclipboard">OleIsCurrentClipboard</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a>
