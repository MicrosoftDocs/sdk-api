---
UID: NF:netcon.INetConnection.GetProperties
title: INetConnection::GetProperties
author: windows-driver-content
description: The GetProperties method retrieves a structure that contains the properties for this network connection.
old-location: ics\inetconnection_getproperties.htm
old-project: ICS
ms.assetid: ab27a7fd-061f-4ea2-8ce8-23d59957a46f
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: GetProperties, GetProperties method [ICS/ICF], GetProperties method [ICS/ICF],INetConnection interface, INetConnection interface [ICS/ICF],GetProperties method, INetConnection.GetProperties, INetConnection::GetProperties, _ics_inetconnection_getproperties, ics.inetconnection_getproperties, netcon/INetConnection::GetProperties
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Hnetcfg.dll
api_name:
-	INetConnection.GetProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetConnection::GetProperties


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>GetProperties</b> method retrieves a structure that contains the properties for this network connection.


## -parameters




### -param ppProps [out]

Pointer to a pointer that, on successful return, points to a 
<a href="https://msdn.microsoft.com/5acda2b8-960f-41ef-9ff2-49787f4e1c0c">NETCON_PROPERTIES</a> structure that contains the properties for this network connection.


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



The calling application should free the memory occupied by the 
<a href="https://msdn.microsoft.com/5acda2b8-960f-41ef-9ff2-49787f4e1c0c">NETCON_PROPERTIES</a> structure returned by <b>GetProperties</b>. Free the memory by calling the <a href="https://msdn.microsoft.com/ac73b831-81da-48e7-858b-7ca1ee03768e">NcFreeNetconProperties</a> function. This function is defined in NetCon.h and is exported by NetShell.dll.




## -see-also




<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

