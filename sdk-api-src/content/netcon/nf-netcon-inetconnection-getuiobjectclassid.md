---
UID: NF:netcon.INetConnection.GetUiObjectClassId
title: INetConnection::GetUiObjectClassId method
author: windows-driver-content
description: The GetUiObjectClassId method retrieves the class identifier of the user interface object for this connection.
old-location: ics\inetconnection_getuiobjectclassid.htm
old-project: ICS
ms.assetid: 33d69dff-8137-4901-9529-31130803b19f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetUiObjectClassId method [ICS/ICF], GetUiObjectClassId method [ICS/ICF], INetConnection interface, GetUiObjectClassId,INetConnection.GetUiObjectClassId, INetConnection, INetConnection interface [ICS/ICF], GetUiObjectClassId method, INetConnection::GetUiObjectClassId, _ics_inetconnection_getuiobjectclassid, ics.inetconnection_getuiobjectclassid, netcon/INetConnection::GetUiObjectClassId
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
-	INetConnection.GetUiObjectClassId
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# INetConnection::GetUiObjectClassId method


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>GetUiObjectClassId</b> method retrieves the class identifier of the user interface object for this connection.


## -parameters




### -param pclsid [out]

Pointer to a <b>CLSID</b> variable that, on successful return, points to the class identifier of the user interface object for this connection.


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
 




## -see-also




<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

