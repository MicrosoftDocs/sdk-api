---
UID: NF:natupnp.INATEventManager.put_NumberOfEntriesCallback
title: INATEventManager::put_NumberOfEntriesCallback
author: windows-driver-content
description: The put_NumberOfEntriesCallback method enables the NAT application with UPnP technology to register a callback interface with the NAT. The system calls the first method in this callback interface if the number of NAT port mappings changes.
old-location: ics\inateventmanager_put_numberofentriescallback.htm
old-project: ICS
ms.assetid: a02a0f1e-5085-444b-adc4-c3cd919f7e25
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: INATEventManager interface [ICS/ICF],put_NumberOfEntriesCallback method, INATEventManager.put_NumberOfEntriesCallback, INATEventManager::put_NumberOfEntriesCallback, _ics_inateventmanager_put_numberofentriescallback, ics.inateventmanager_put_numberofentriescallback, natupnp/INATEventManager::put_NumberOfEntriesCallback, put_NumberOfEntriesCallback, put_NumberOfEntriesCallback method [ICS/ICF], put_NumberOfEntriesCallback method [ICS/ICF],INATEventManager interface
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SystemHealthAgentState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Hnetcfg.dll
api_name:
-	INATEventManager.put_NumberOfEntriesCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INATEventManager::put_NumberOfEntriesCallback


## -description


The <b>put_NumberOfEntriesCallback</b> method enables the NAT application with UPnP technology to register a callback interface with the NAT. The system calls the first method in this callback interface if the number of NAT port mappings changes.


## -parameters




### -param pUnk [in]

Pointer to an object that supports either the 
<a href="_com_iunknown">IUnknown</a> interface or the 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. See the Remarks section for more information.


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



The object referred to by <i>pUnk</i> must either support the 
<a href="https://msdn.microsoft.com/c64e5ce3-78f6-4f51-8ae1-c871c4716d26">INATNumberOfEntriesCallback</a> interface or the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. The NAT first queries <i>pUnk</i> for the 
<b>INATNumberOfEntriesCallback</b> interface. If this interface is not supported, the NAT queries <i>pUnk</i> for the <b>IDispatch</b> interface. If the <b>IDispatch</b> interface is not supported, the <b>NumberOfEntriesCallback</b> method returns E_FAIL.

If only <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> is supported, the NAT invokes the callback by calling <a href="964ade8e-9d8a-4d32-bd47-aa678912a54d">IDispatch::Invoke</a> with the dispatch ID specified as zero, which indicates the default method. This <b>IDispatch</b> method is passed the same parameters as the 
<a href="https://msdn.microsoft.com/c64e5ce3-78f6-4f51-8ae1-c871c4716d26">INATNumberOfEntriesCallback</a> method, except that the first parameter passed is a string that indicates the reason the callback is invoked.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/18c5df1a-e57e-4f44-bac5-a5861f939673">INATEventManager</a>



<a href="https://msdn.microsoft.com/c64e5ce3-78f6-4f51-8ae1-c871c4716d26">INATNumberOfEntriesCallback</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

