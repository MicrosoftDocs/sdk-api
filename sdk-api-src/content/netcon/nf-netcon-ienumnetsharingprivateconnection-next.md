---
UID: NF:netcon.IEnumNetSharingPrivateConnection.Next
title: IEnumNetSharingPrivateConnection::Next
author: windows-sdk-content
description: The Next method retrieves the specified number of privately-shared connections that start from the current enumeration position.
old-location: ics\ienumnetsharingprivateconnection_next.htm
old-project: ICS
ms.assetid: 3f9cc481-8967-4b1e-95b2-c6ddec20a1ea
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IEnumNetSharingPrivateConnection interface [ICS/ICF],Next method, IEnumNetSharingPrivateConnection.Next, IEnumNetSharingPrivateConnection::Next, Next, Next method [ICS/ICF], Next method [ICS/ICF],IEnumNetSharingPrivateConnection interface, _ics_ienumnetsharingprivateconnection_next, ics.ienumnetsharingprivateconnection_next, netcon/IEnumNetSharingPrivateConnection::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - IEnumNetSharingPrivateConnection.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumNetSharingPrivateConnection::Next


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>Next</b> method retrieves the specified number of privately-shared connections that start from the current enumeration position.


## -parameters




### -param celt [in]

Specifies the number of privately-shared connections to retrieve.


### -param rgVar [out]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> variable for the connection. This variant contains a pointer to an 
<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a> interface.


### -param pCeltFetched






#### - pceltFetched [out]

Pointer to a <b>ULONG</b> variable that, on successful return, specifies the number of privately-shared connections actually returned.


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
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/0e4cfa2e-8caa-4258-bd52-1f5a00403dfa">IEnumNetSharingPrivateConnection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

