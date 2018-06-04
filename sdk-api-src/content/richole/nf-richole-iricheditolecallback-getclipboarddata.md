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

# IRichEditOleCallback::GetClipboardData


## -description


Allows the client to supply its own clipboard object.


## -parameters




### -param lpchrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a>*</b>

The clipboard object range. 


### -param reco

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


   The clipboard operation flag can be one of these values.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECO_COPY"></a><a id="reco_copy"></a><dl>
<dt><b>RECO_COPY</b></dt>
</dl>
</td>
<td width="60%">
Copy to the clipboard.

</td>
</tr>
<tr>
<td width="40%"><a id="RECO_CUT"></a><a id="reco_cut"></a><dl>
<dt><b>RECO_CUT</b></dt>
</dl>
</td>
<td width="60%">
Cut to the clipboard.

</td>
</tr>
</table>
 


### -param lplpdataobj

Type: <b>LPDATAOBJECT*</b>

Pointer to the pointer variable that receives the address of the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> implementation representing the range specified in the 
					<i>lpchrg</i> parameter. The value of 
					<i>lplpdataobj</i> is ignored if an error is returned. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the return value is <b>E_NOTIMPL</b>, the rich edit control created its own clipboard object. If the return value is a failure other than <b>E_NOTIMPL</b>, the operation failed.




## -see-also




<a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a>



<a href="https://msdn.microsoft.com/2c3ba341-f62f-4c95-9547-6d50fcf3d6b4">IRichEditOleCallback</a>



<b>Reference</b>
 

 

