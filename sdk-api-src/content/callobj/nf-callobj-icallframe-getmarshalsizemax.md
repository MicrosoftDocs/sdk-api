---
UID: NF:callobj.ICallFrame.GetMarshalSizeMax
title: ICallFrame::GetMarshalSizeMax
author: windows-sdk-content
description: Retrieves an upper bound on the number of bytes needed to marshal the call frame.
old-location: com\icallframe_getmarshalsizemax.htm
tech.root: com
ms.assetid: 4e564b29-8b21-4e65-981e-4ceda1d7774d
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetMarshalSizeMax, GetMarshalSizeMax method [COM], GetMarshalSizeMax method [COM],ICallFrame interface, ICallFrame interface [COM],GetMarshalSizeMax method, ICallFrame.GetMarshalSizeMax, ICallFrame::GetMarshalSizeMax, _com_icallframe_getmarshalsizemax, callobj/ICallFrame::GetMarshalSizeMax, com.icallframe_getmarshalsizemax
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame.GetMarshalSizeMax
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallFrame::GetMarshalSizeMax


## -description


Retrieves an upper bound on the number of bytes needed to marshal the call frame.

Usually an interface proxy calls this method to learn how big a buffer is needed, allocates the buffer, and then calls the <a href="https://msdn.microsoft.com/en-us/library/ms693325(v=VS.85).aspx">Marshal</a> method to carry out the marshalling.


## -parameters




### -param pmshlContext [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms682388(v=VS.85).aspx">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how marshalling is carried out.


### -param mshlflags [in]

Indicates whether the data to be marshaled is to be transmitted back to the client process â€” the normal case â€” or written to a global table, where it can be retrieved by multiple clients. For a list of values, see the <a href="https://msdn.microsoft.com/en-us/library/ms680759(v=VS.85).aspx">MSHLFLAGS</a> enumeration.


### -param pcbBufferNeeded [out]

A pointer to the size of the buffer, in bytes, that will be needed to marshal the call frame.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms683709(v=VS.85).aspx">ICallFrame</a>
 

 

