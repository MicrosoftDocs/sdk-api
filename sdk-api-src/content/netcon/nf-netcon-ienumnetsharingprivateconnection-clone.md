---
UID: NF:netcon.IEnumNetSharingPrivateConnection.Clone
title: IEnumNetSharingPrivateConnection::Clone
author: windows-sdk-content
description: The Clone method creates a new enumeration interface from this enumeration.
old-location: ics\ienumnetsharingprivateconnection_clone.htm
tech.root: ICS
ms.assetid: a82dbc70-783a-4061-9526-dd19f94d843b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Clone, Clone method [ICS/ICF], Clone method [ICS/ICF],IEnumNetSharingPrivateConnection interface, IEnumNetSharingPrivateConnection interface [ICS/ICF],Clone method, IEnumNetSharingPrivateConnection.Clone, IEnumNetSharingPrivateConnection::Clone, _ics_ienumnetsharingprivateconnection_clone, ics.ienumnetsharingprivateconnection_clone, netcon/IEnumNetSharingPrivateConnection::Clone
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
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - IEnumNetSharingPrivateConnection.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumNetSharingPrivateConnection::Clone


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>Clone</b> method creates a new enumeration interface from this enumeration.


## -parameters




### -param ppenum [out]

Pointer to an interface pointer that, on successful return, points to an 
<a href="https://msdn.microsoft.com/0e4cfa2e-8caa-4258-bd52-1f5a00403dfa">IEnumNetSharingPrivateConnection</a> interface.


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




<a href="https://msdn.microsoft.com/0e4cfa2e-8caa-4258-bd52-1f5a00403dfa">IEnumNetSharingPrivateConnection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

