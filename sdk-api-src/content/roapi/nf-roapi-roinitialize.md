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

# RoInitialize function


## -description


Initializes the Windows Runtime on the current thread with the specified concurrency model.


## -parameters




### -param initType [in]

Type: <b><a href="https://msdn.microsoft.com/961ABFEB-E11F-4405-A021-F3756A79AF18">RO_INIT_TYPE</a></b>

The concurrency model for the thread. The default is <b>RO_INIT_MULTITHREADED</b>.


## -returns



Type: <b>HRESULT</b>

This function can return the standard return values <b>E_INVALIDARG</b>, <b>E_OUTOFMEMORY</b>, and <b>E_UNEXPECTED</b>, as well as the following values.

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
The Windows Runtime was initialized successfully on this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The Windows Runtime is already initialized on this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CHANGED_MODE</b></dt>
</dl>
</td>
<td width="60%">
A previous call to <a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a> specified the concurrency model for this thread as multithread apartment (MTA). This could also indicate that a change from neutral-threaded apartment to single-threaded apartment has occurred.

</td>
</tr>
</table>
 




## -remarks



Use the <b>RoInitialize</b> function to initialize a thread in the Windows Runtime. All threads that activate and interact with Windows Runtime objects must be initialized prior to calling into the Windows Runtime. 

Call the <a href="https://msdn.microsoft.com/0F910E71-BA44-44A6-8432-52A4E38854F9">RoUninitialize</a> function to close the Windows Runtime on the current thread. Each successful call to <b>RoInitialize</b>, including those that return <b>S_FALSE</b>, must be balanced by a corresponding call to <b>RoUninitialize</b>.




## -see-also




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>



<a href="https://msdn.microsoft.com/961ABFEB-E11F-4405-A021-F3756A79AF18">RO_INIT_TYPE</a>



<a href="https://msdn.microsoft.com/0F910E71-BA44-44A6-8432-52A4E38854F9">RoUninitialize</a>
 

 

