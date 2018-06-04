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

# IShellWindows::FindWindowSW


## -description


Finds a window in the Shell windows collection and returns the window's handle and <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface.


## -parameters




### -param pvarLoc [in]

Type: <b>VARIANT*</b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> of type VT_VARIANT | VT_BYREF. Set the value of <i>pvarLoc</i> to an absolute <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">PIDL</a> (PIDLIST_ABSOLUTE) that specifies the window to find. (See remarks.)


### -param pvarLocRoot [in]

Type: <b>VARIANT*</b>

Must be <b>NULL</b> or of type VT_EMPTY.


### -param swClass [in]

Type: <b>int</b>

One or more <a href="https://msdn.microsoft.com/79d4fcf3-5256-4e21-ab9a-94605e1d742f">ShellWindowTypeConstants</a> flags that specify window types to include in the search.


### -param phwnd [out]

Type: <b>long*</b>

A handle for the window matching the specified search criteria, or <b>NULL</b> if no such window was found.


### -param swfwOptions

Type: <b>int</b>

One or more <a href="https://msdn.microsoft.com/2459ab16-56c0-4812-bc61-4a17978b04f3">ShellWindowFindWindowOptions</a> flags that specify search options.


### -param ppdispOut [out, retval]

Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>**</b>

A reference to the window's <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface, or <b>NULL</b> if no such window was found.


## -returns



Type: <b>HRESULT</b>

One of the following values, or a standard result code.

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
A window matching the specified search criteria was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
A window matching the specified search criteria was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A window was found, but a reference to the window's <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface could not be obtained. Only occurs if the <a href="https://msdn.microsoft.com/2459ab16-56c0-4812-bc61-4a17978b04f3">SWFO_NEEDDISPATCH</a> flag is set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
A window was found, but the window is pending open. Only occurs if the <a href="https://msdn.microsoft.com/2459ab16-56c0-4812-bc61-4a17978b04f3">SWFO_INCLUDEPENDING</a> flag is set.

</td>
</tr>
</table>
 




## -remarks



If the <a href="https://msdn.microsoft.com/2459ab16-56c0-4812-bc61-4a17978b04f3">SWFO_COOKIEPASSED</a> flag is set, <i>pvarLoc</i> is interpreted as a cookie instead of a PIDL.



