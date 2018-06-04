---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITextServices::TxGetText


## -description


Returns all of the Unicode plain text in the control as a <b>BSTR</b>.


## -parameters




### -param pbstrText

Type: <b>
            BSTR
          *</b>

The Unicode plain text. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the text is successfully returned in the output argument, the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following <b>HRESULT</b> codes. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Invalid <b>BSTR</b> pointer passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate memory for copy of the text.

</td>
</tr>
</table>
 




## -remarks



The host (caller) takes ownership of the returned <b>BSTR</b>.

Other ways to retrieve plain text data are to use <a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a> or the Text Object Model (TOM) <a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a> method.

If there is no text in the control, the <b>BSTR</b> is allocated and 0x000D is returned in it.

The returned text will <i>not</i> necessarily be null-terminated.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

