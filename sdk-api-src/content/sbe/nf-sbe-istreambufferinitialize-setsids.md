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

# IStreamBufferInitialize::SetSIDs


## -description


The <b>SetSIDs</b> method sets the security identifiers (SIDs) that are used to protect access to the backing files.


## -parameters




### -param cSIDs [in]

Specifies the size of the array given in the <i>ppSID</i> parameter.


### -param ppSID [in]

Pointer to an array of <b>SID</b> structures, of size <i>cSIDs</i>.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

</td>
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
</table>
 




## -remarks



At run time, the Stream Buffer Source and Sink filters create various Win32 objects, such as mutexes, so that access to the backing files is synchronized across threads. Each of the filters maintains a list of SIDs that are used to protect these objects. By default, the filters inherit their SIDs from the hosting process. An application can use the <b>SetSIDs</b> method to override the default SIDs.

If you call this method, do so before locking the sink filter or loading a file in the source filter. It is recommended that all of the filters be given the same SIDs.

<ul>
<li>
<div class="alert"><b>Important</b>  
             Setting less-privileged SIDs can create a security issue.</div>
<div> </div>
</li>
</ul>
Note that this method does not apply to content recording files, which are protected by the discretionary access-control lists (DACLs) of the directory structure.




## -see-also




<a href="https://msdn.microsoft.com/357b2979-78de-4a99-bf52-4117af7dfaad">IStreamBufferInitialize Interface</a>
 

 

