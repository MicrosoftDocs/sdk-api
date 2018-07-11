---
UID: NF:natupnp.INATNumberOfEntriesCallback.NewNumberOfEntries
title: INATNumberOfEntriesCallback::NewNumberOfEntries
author: windows-sdk-content
description: The system calls the NewNumberOfEntries method if the total number of NAT port mappings changes.
old-location: ics\inatnumberofentriescallback_newnumberofentries.htm
old-project: ics
ms.assetid: 55998538-ddce-4a83-8d21-387f3c1f3b6a
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: INATNumberOfEntriesCallback interface [ICS/ICF],NewNumberOfEntries method, INATNumberOfEntriesCallback.NewNumberOfEntries, INATNumberOfEntriesCallback::NewNumberOfEntries, NewNumberOfEntries, NewNumberOfEntries method [ICS/ICF], NewNumberOfEntries method [ICS/ICF],INATNumberOfEntriesCallback interface, _ics_inatnumberofentriescallback_newnumberofentries, ics.inatnumberofentriescallback_newnumberofentries, natupnp/INATNumberOfEntriesCallback::NewNumberOfEntries
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: natupnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SystemHealthAgentState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INATNumberOfEntriesCallback.NewNumberOfEntries
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INATNumberOfEntriesCallback::NewNumberOfEntries


## -description


The system calls the 
<b>NewNumberOfEntries</b> method if the total number of NAT port mappings changes.


## -parameters




### -param lNewNumberOfEntries [in]

Specifies a <b>long</b> variable that contains the new number of port mappings.


## -returns



If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



The system calls this method when the total number of port mappings changes. The change in the total number of port mappings may be the result of a change in the number of dynamic port mappings. In this case, the system calls this method even though the number of static port mappings has not changed.




## -see-also




<a href="https://msdn.microsoft.com/a02a0f1e-5085-444b-adc4-c3cd919f7e25">INATEventManager::put_NumberOfEntriesCallback</a>



<a href="https://msdn.microsoft.com/c64e5ce3-78f6-4f51-8ae1-c871c4716d26">INATNumberOfEntriesCallback</a>



<a href="https://msdn.microsoft.com/8ececd98-a700-4d64-8f89-a1ec36597edf">IStaticPortMappingCollection::get_Count</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

