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

# IWMReaderAdvanced::SetClientInfo


## -description



The <b>SetClientInfo</b> method sets client-side information used for logging. Use this method to specify information about the client that the reader object sends to the server for logging. If the application does not call this method, the reader object uses default values.




## -parameters




### -param pClientInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/9c8d1534-976d-4a9e-9c89-368e1a11bd26">WM_READER_CLIENTINFO</a> structure allocated by the caller, which contains information about the client.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. The <b>cbSize</b> member must be set, and the string values must not exceed 1024 characters.

</td>
</tr>
</table>
 




## -remarks



Initialize the <b>WM_READER_CLIENTINFO</b> structure before calling this method. Always set the <b>cbSize</b> member equal to the size of the structure, and set any unused fields to zero.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
WM_READER_CLIENTINFO info;
ZeroMemory(&amp;info, sizeof(WM_READER_CLIENTINFO));
info.cbSize = sizeof(WM_READER_CLIENTINFO);

// Set other fields (not shown).

hr = pReaderAdvanced-&gt;SetClientInfo( &amp;info );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3e0d0fea-4370-41f8-b461-73a37de8d8bc">Client Logging</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>
 

 

