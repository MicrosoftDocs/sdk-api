---
UID: NF:richole.IRichEditOle.ImportDataObject
title: IRichEditOle::ImportDataObject
author: windows-sdk-content
description: Imports a clipboard object into a rich edit control, replacing the current selection.
old-location: controls\IRichEditOle_ImportDataObject.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleimportdataobject.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IRichEditOle interface [Windows Controls],ImportDataObject method, IRichEditOle.ImportDataObject, IRichEditOle::ImportDataObject, ImportDataObject, ImportDataObject method [Windows Controls], ImportDataObject method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_ImportDataObject, _win32_IRichEditOle_ImportDataObject_cpp, controls.IRichEditOle_ImportDataObject, controls._win32_IRichEditOle_ImportDataObject, richole/IRichEditOle::ImportDataObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TEXTRANGEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOle.ImportDataObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: ADAM
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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HGLOBAL</a></b>

Handle to a metafile containing the icon view of an object. The handle is used only if the <b>DVASPECT_ICON</b> display aspect is required by a <a href="_ole_OleUIPasteSpecial">Paste Special</a> operation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

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




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>
 

 

