---
UID: NF:p2p.PeerGraphGetNextItem
title: PeerGraphGetNextItem function
author: windows-sdk-content
description: Obtains the next item or items in an enumeration created by a call to the following functions.
old-location: p2p\peergraphgetnextitem.htm
tech.root: p2psdk
ms.assetid: f595e66d-570f-4642-bef8-ff5cf070649c
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PeerGraphGetNextItem, PeerGraphGetNextItem function [Peer Networking], p2p.peergraphgetnextitem, p2p/PeerGraphGetNextItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphGetNextItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGraphGetNextItem function


## -description


The <b>PeerGraphGetNextItem</b> function obtains the next item or items in an enumeration created by a call to the following functions, which return a peer enumeration handle:  <ul>
<li>
<a href="https://msdn.microsoft.com/ef4ea3e2-fd71-48d8-a9a8-db38ef06df20">PeerGraphEnumConnections</a>
</li>
<li>
<a href="https://msdn.microsoft.com/68231b0a-6002-4974-84d7-08b0629f3622">PeerGraphEnumNodes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0f20c738-ae56-4352-a1fb-5aa469a58bc8">PeerGraphSearchRecords</a>
</li>
</ul>

## -parameters




### -param hPeerEnum [in]

Handle to an enumeration.


### -param pCount [in, out]

Input specifies the number of items to obtain.

Output receives the actual number of items obtained.

<div class="alert"><b>Note</b>  If <i>pCount</i> is a zero (0) output, the end of the enumeration is reached.</div>
<div> </div>

### -param pppvItems [out]

Receives an array of pointers to  the requested items.  The number  of pointers contained in an array is specified by the output value of  <i>pCount</i>.  The actual data returned depends on the type of enumeration. The  types of structures that are returned are the following:  <a href="https://msdn.microsoft.com/039fa00e-c193-46fd-b7e6-41eb7baeab3e">PEER_CONNECTION_INFO</a>, <a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a>, and <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a>



## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

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
One parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



 Free  <i>ppvItems</i> by calling <a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a> when the data is no longer required.

The application can request a range of items to obtain.   The function  returns <i>pCount</i> or fewer items.


#### Examples

The following code snippet shows you how to  use  <b>PeerGraphGetNextItem</b> to enumerate objects, and end an enumeration after you finish processing the enumeration.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//PeerGraphGetNextItem snippet
    // hPeerEnum is a handle to the enumeration obtained from a successful call to PeerGraphEnumConnections,
    // PeerGraphEnumNodes, PeerGraphEnumRecords, or PeerGraphSearchRecords.
    // Set count equal to the maximum number of items you want returned. To obtain a count of all the items
    // in the enumeration, call PeerGraphGetItemCount.
    // ppRecord is an array of pointers to PEER_RECORD objects.  PEER_CONNECTION_INFO and PEER_NODE_INFO structures
    // are also supported.
    HRESULT hr = PeerGraphGetNextItem(hPeerEnum, &amp;count, (PVOID *)&amp;ppRecord);
    if (FAILED(hr))
    {
        // Insert your code to handle the error here.
    }
    else
    {
        // Free the data obtained by PeerGraphGetNextItem.
        PeerGraphFreeData(ppRecord);
    }

    // If you are done with the enumeration, free the handle to the enumeration.
    PeerGraphEndEnumeration(hPeerEnum);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/039fa00e-c193-46fd-b7e6-41eb7baeab3e">PEER_CONNECTION_INFO</a>



<a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a>



<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a>



<a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>



<a href="https://msdn.microsoft.com/ef4ea3e2-fd71-48d8-a9a8-db38ef06df20">PeerGraphEnumConnections</a>



<a href="https://msdn.microsoft.com/68231b0a-6002-4974-84d7-08b0629f3622">PeerGraphEnumNodes</a>



<a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a>



<a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a>



<a href="https://msdn.microsoft.com/0f20c738-ae56-4352-a1fb-5aa469a58bc8">PeerGraphSearchRecords</a>
 

 

