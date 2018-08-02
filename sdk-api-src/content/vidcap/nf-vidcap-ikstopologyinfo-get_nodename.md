---
UID: NF:vidcap.IKsTopologyInfo.get_NodeName
title: IKsTopologyInfo::get_NodeName
author: windows-sdk-content
description: The get_NodeName method returns the name of the node.
old-location: dshow\ikstopologyinfo_get_nodename.htm
old-project: DirectShow
ms.assetid: 3e24ef6f-e49d-4397-a9b8-a46fcf576a01
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NodeName method, IKsTopologyInfo.get_NodeName, IKsTopologyInfo::get_NodeName, IKsTopologyInfoget_NodeName, dshow.ikstopologyinfo_get_nodename, get_NodeName, get_NodeName method [DirectShow], get_NodeName method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NodeName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo.get_NodeName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IKsTopologyInfo::get_NodeName


## -description


The <code>get_NodeName</code> method returns the name of the node.


## -parameters




### -param dwNodeId [in]

Index of the node. To find the number of nodes, call the <a href="https://msdn.microsoft.com/fdba99d5-fd44-4d4f-8575-867d98bf3339">IKsTopologyInfo::get_NumNodes</a> method.


### -param pwchNodeName [out]

Pointer to a wide-character array that receives the name. To find the required buffer size, set this parameter to <b>NULL</b>. The size is returned in the <i>pdwNameLen</i> parameter.


### -param dwBufSize [in]

Size of the <i>pwchNodeName</i> array, in bytes.


### -param pdwNameLen [out]

Receives the buffer size required to hold the name, in bytes. This parameter cannot be <b>NULL</b>.


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
<dt><b>WIN32_FROM_HRESULT(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough.

</td>
</tr>
</table>
 




## -remarks



To find the buffer size for the name, call the method once with <b>NULL</b> for the <i>pwchNodeName</i> parameter and zero for the <i>dwBufSize</i> parameter. The method returns the buffer size in <i>pdwNameLen</i>. The method's return value, in this case, is HRESULT_FROM_WIN32(ERROR_MORE_DATA). Then allocate the array and call the method again.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// pKsTopo is an IKsTopologyInfo pointer.
// iNode is the index of a node.
DWORD cbName = 0;
hr = pKsTopo-&gt;get_NodeName(iNode, NULL, 0, &amp;cbName);
if (hr == HRESULT_FROM_WIN32(ERROR_MORE_DATA))
{
    if (cbName &gt; sizeof(WCHAR))
    {
        WCHAR *nodeName = new WCHAR[cbName / sizeof(WCHAR)];
        if (nodeName == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            hr = pKsTopo-&gt;get_NodeName(iNode, nodeName, cbName, &amp;cbName);
            /* ... */
            delete [] nodeName;
        }
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo Interface</a>
 

 

