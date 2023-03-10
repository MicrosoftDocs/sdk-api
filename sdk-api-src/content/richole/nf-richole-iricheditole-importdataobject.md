---
UID: NF:richole.IRichEditOle.ImportDataObject
title: IRichEditOle::ImportDataObject (richole.h)
description: Imports a clipboard object into a rich edit control, replacing the current selection.
helpviewer_keywords: ["IRichEditOle interface [Windows Controls]","ImportDataObject method","IRichEditOle.ImportDataObject","IRichEditOle::ImportDataObject","ImportDataObject","ImportDataObject method [Windows Controls]","ImportDataObject method [Windows Controls]","IRichEditOle interface","_win32_IRichEditOle_ImportDataObject","_win32_IRichEditOle_ImportDataObject_cpp","controls.IRichEditOle_ImportDataObject","controls._win32_IRichEditOle_ImportDataObject","richole/IRichEditOle::ImportDataObject"]
old-location: controls\IRichEditOle_ImportDataObject.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleimportdataobject.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],ImportDataObject method, IRichEditOle.ImportDataObject, IRichEditOle::ImportDataObject, ImportDataObject, ImportDataObject method [Windows Controls], ImportDataObject method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_ImportDataObject, _win32_IRichEditOle_ImportDataObject_cpp, controls.IRichEditOle_ImportDataObject, controls._win32_IRichEditOle_ImportDataObject, richole/IRichEditOle::ImportDataObject
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditOle::ImportDataObject
 - richole/IRichEditOle::ImportDataObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOle.ImportDataObject
---

# IRichEditOle::ImportDataObject


## -description

Imports a clipboard object into a rich edit control, replacing the current selection.

## -parameters

### -param lpdataobj

Type: <b>LPDATAOBJECT</b>

The clipboard object to import.

### -param cf

Type: <b>CLIPFORMAT</b>

Clipboard format to use. A value of zero will use the best available format.

### -param hMetaPict

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HGLOBAL</a></b>

Handle to a metafile containing the icon view of an object. The handle is used only if the <b>DVASPECT_ICON</b> display aspect is required by a <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuipastespeciala">Paste Special</a> operation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the method fails, it can return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
There was an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to do the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>