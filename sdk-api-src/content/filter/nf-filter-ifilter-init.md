---
UID: NF:filter.IFilter.Init
title: IFilter::Init
author: windows-sdk-content
description: Initializes a filtering session.
old-location: indexsrv\ifilter_init.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_2oc4.htm
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IFilter interface [Indexing Service],Init method, IFilter.Init, IFilter::Init, Init, Init method [Indexing Service], Init method [Indexing Service],IFilter interface, _idxs_IFilter_Init, filter/IFilter::Init, indexsrv.ifilter_init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: filter.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Filter.h
api_name:
 - IFilter.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- filter.h
: 
- IFilter.Init
: 
---

# IFilter::Init


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Initializes a filtering session.


## -parameters




### -param grfFlags [in]

Values from the <a href="https://msdn.microsoft.com/en-us/library/ms691091(v=VS.85).aspx">IFILTER_INIT</a> enumeration for controlling text standardization, property output, embedding scope, and <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a> access patterns. 


### -param cAttributes [in]

The size of the attributes array. When nonzero, <i>cAttributes</i> takes precedence over attributes specified in <i>grfFlags</i>. If no attribute flags are specified and <i>cAttributes</i> is zero, the default is given by the PSGUID_STORAGE storage property set, which contains the date and time of the last write to the file, size, and so on; and by the PID_STG_CONTENTS 'contents' property, which maps to the main contents of the file. For more information about properties and property sets, see <a href="https://msdn.microsoft.com/en-us/library/ms691041(v=VS.85).aspx">Property Sets</a>.


### -param aAttributes [in]

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms690996(v=VS.85).aspx">FULLPROPSPEC</a> structures for the requested properties. When <i>cAttributes</i> is nonzero, only the properties in <i>aAttributes</i> are returned. 


### -param pFlags [out]

Information about additional properties available to the caller; from the <a href="https://msdn.microsoft.com/en-us/library/ms690831(v=VS.85).aspx">IFILTER_FLAGS</a> enumeration. 


## -returns



This method can return one of these values.

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
<dt><b>E_FAIL 
</b></dt>
</dl>
</td>
<td width="60%">
File to filter was not previously loaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
Count and contents of attributes do not agree.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_PASSWORD </b></dt>
</dl>
</td>
<td width="60%">
Access has been denied because of password protection or similar security measures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_ACCESS </b></dt>
</dl>
</td>
<td width="60%">
General access failures

</td>
</tr>
</table>
 




## -remarks



The <b>Init</b> method sets the state of the filter object. The content filter positions at the beginning of the object and the object state is frozen until the object is released. You can pass the filter object the set of properties you would like returned by setting up their property set and property identifier (ID) descriptions in the <i>aAttributes</i> array. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms692552(v=VS.85).aspx">Filtering File Properties</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call the <b>Init</b> method before calling all other <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a> methods.



<h3><a id="Notes_to_Implementers_"></a><a id="notes_to_implementers_"></a><a id="NOTES_TO_IMPLEMENTERS_"></a>Notes to Implementers
</h3>
Chunk IDs must remain consistent across multiple calls to the <b>Init</b> method with the same parameters. 

For some implementations of the <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a> interface, detection of failure to access a document may not be possible (or may be computationally expensive) until the <b>Init</b> method has been called, or possibly even later. 






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690996(v=VS.85).aspx">FULLPROPSPEC</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690831(v=VS.85).aspx">IFILTER_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691091(v=VS.85).aspx">IFILTER_INIT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a>
 

 

