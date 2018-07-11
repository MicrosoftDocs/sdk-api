---
UID: NF:richole.IRichEditOle.GetClipboardData
title: IRichEditOle::GetClipboardData
author: windows-sdk-content
description: Retrieves a clipboard object for a range in an edit control.
old-location: controls\IRichEditOle_GetClipboardData.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolegetclipboarddata.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetClipboardData, GetClipboardData method [Windows Controls], GetClipboardData method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],GetClipboardData method, IRichEditOle.GetClipboardData, IRichEditOle::GetClipboardData, _win32_IRichEditOle_GetClipboardData, _win32_IRichEditOle_GetClipboardData_cpp, controls.IRichEditOle_GetClipboardData, controls._win32_IRichEditOle_GetClipboardData, richole/IRichEditOle::GetClipboardData
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
 - IRichEditOle.GetClipboardData
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: ADAM
---

# IRichEditOle::GetClipboardData


## -description


Retrieves a clipboard object for a range in an edit control.


## -parameters




### -param lpchrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a>*</b>

The range for which to create the clipboard object. 


### -param reco

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Unused.


### -param lplpdataobj

Type: <b>LPDATAOBJECT*</b>

The <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface of the clipboard object representing the range specified in the 
					<i>lpchrg</i> parameter.


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




<a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a>



<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>



<b>Reference</b>
 

 

