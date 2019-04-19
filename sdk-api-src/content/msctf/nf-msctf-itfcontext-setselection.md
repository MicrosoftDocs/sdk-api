---
UID: NF:msctf.ITfContext.SetSelection
title: ITfContext::SetSelection (msctf.h)
author: windows-sdk-content
description: ITfContext::SetSelection method
old-location: tsf\itfcontext_setselection.htm
tech.root: TSF
ms.assetid: 1cf50b5e-6ec2-4649-9acc-743a2e3d8096
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfContext interface [Text Services Framework],SetSelection method, ITfContext.SetSelection, ITfContext::SetSelection, SetSelection, SetSelection method [Text Services Framework], SetSelection method [Text Services Framework],ITfContext interface, _tsf_itfcontext_setselection_ref, msctf/ITfContext::SetSelection, tsf.itfcontext_setselection
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContext.SetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContext::SetSelection


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param ulCount [in]

Specifies the number of selections in the <i>pSelection</i> array.


### -param pSelection [in]

An array of <a href="https://msdn.microsoft.com/c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54">TF_SELECTION</a> structures that contain the information for each selection.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
The document has no selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The cookie in <i>ec</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



A selection is a span of highlighted text, or an insertion point if the span is empty, identifying the user focus area within a document. Some documents are capable of having multiple selections. There can only be one zero-length selection in <i>pSelection</i> as it represents the position of the document caret.

If an application must adjust the text covered by a selection, it should wait until the caller releases the lock. However, applications can adjust any of the <b>style</b> members of the <b>TF_SELECTION</b> structures while still returning S_OK.

The caller can set the <b>fInterimChar</b> flag only if one selection is set. In this case, the selection should span exactly one character and the <b>ase</b> member of the <b>TF_SELECTION</b> structure is set to TFAE_NONE.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54">TF_SELECTION
      </a>
 

 

