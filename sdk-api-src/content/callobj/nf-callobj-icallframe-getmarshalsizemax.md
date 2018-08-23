---
UID: NF:callobj.ICallFrame.GetMarshalSizeMax
title: ICallFrame::GetMarshalSizeMax
author: windows-sdk-content
description: Retrieves an upper bound on the number of bytes needed to marshal the call frame.
old-location: com\icallframe_getmarshalsizemax.htm
old-project: com
ms.assetid: 4e564b29-8b21-4e65-981e-4ceda1d7774d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMarshalSizeMax, GetMarshalSizeMax method [COM], GetMarshalSizeMax method [COM],ICallFrame interface, ICallFrame interface [COM],GetMarshalSizeMax method, ICallFrame.GetMarshalSizeMax, ICallFrame::GetMarshalSizeMax, _com_icallframe_getmarshalsizemax, callobj/ICallFrame::GetMarshalSizeMax, com.icallframe_getmarshalsizemax
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: callobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CALLFRAME_COPY
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
req.lib: 
req.dll: 
req.irql: 
---

# ICallFrame::GetMarshalSizeMax


## -description


Retrieves an upper bound on the number of bytes needed to marshal the call frame.

Usually an interface proxy calls this method to learn how big a buffer is needed, allocates the buffer, and then calls the <a href="https://msdn.microsoft.com/cab40c31-1f89-4da9-a1e0-ef946b34665c">Marshal</a> method to carry out the marshalling.


## -parameters




### -param pmshlContext [in]

A pointer to the <a href="https://msdn.microsoft.com/4ecc4646-db3f-4d0e-9c45-b78a288156e1">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how marshalling is carried out.


### -param mshlflags [in]

Indicates whether the data to be marshaled is to be transmitted back to the client process â€” the normal case â€” or written to a global table, where it can be retrieved by multiple clients. For a list of values, see the <a href="https://msdn.microsoft.com/42a482be-d4b8-4f2e-ae43-1d210cb44c7c">MSHLFLAGS</a> enumeration.


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




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

