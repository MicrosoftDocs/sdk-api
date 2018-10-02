---
UID: NF:ntquery.BindIFilterFromStream
title: BindIFilterFromStream function
author: windows-sdk-content
description: Retrieves the IFilter interface pointer for the specified storage object. This is especially useful when filtering the contents of a document and processing embedded OLE objects accessible through their IStream interfaces.
old-location: indexsrv\bindifilterfromstream.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0f8t.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BindIFilterFromStream, BindIFilterFromStream function [Indexing Service], _idxs_BindIFilterFromStream, indexsrv.bindifilterfromstream, ntquery/BindIFilterFromStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntquery.dll
api_name:
 - BindIFilterFromStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BindIFilterFromStream function


## -description


<p class="CCE_Message">[Indexing Service is unsupported as of Windows XP. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a> interface pointer for the specified storage object. This is especially useful when filtering the contents of a document and processing embedded OLE objects accessible through their <b>IStream</b> interfaces.



## -parameters




### -param pStm [in]

A pointer to the <b>IStream</b> interface to be used to access the file. 


### -param pUnkOuter [in]

A pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the aggregate in which this stream object exists.


### -param ppIUnk [out]

A pointer to an output variable that receives the <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a> interface pointer. 


## -returns



This function can return one of these values.

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
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The function was denied access to the path of the storage object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The function encountered an invalid handle, probably due to a low-memory situation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The function received an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function did not have sufficient memory or other resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unknown error has occurred.

</td>
</tr>
</table>
 




## -remarks



This function is not a full implementation of a COM persistent handler.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690929(v=VS.85).aspx">BindIFilterFromStorage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691002(v=VS.85).aspx">LoadIFilter</a>
 

 

