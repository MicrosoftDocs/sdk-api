---
UID: NF:netcon.INetConnectionProps.get_Name
title: INetConnectionProps::get_Name (netcon.h)
author: windows-sdk-content
description: The get_Name method retrieves the name of the connection.
old-location: ics\inetconnectionprops_get_name.htm
tech.root: ics
ms.assetid: 7ff91c38-51af-467b-baff-0d41a2ba14f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetConnectionProps interface [ICS/ICF],get_Name method, INetConnectionProps.get_Name, INetConnectionProps::get_Name, _ics_inetconnectionprops_get_name, get_Name, get_Name method [ICS/ICF], get_Name method [ICS/ICF],INetConnectionProps interface, ics.inetconnectionprops_get_name, netcon/INetConnectionProps::get_Name
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
 - INetConnectionProps.get_Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetConnectionProps::get_Name


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_Name</b> method retrieves the name of the connection.


## -parameters




### -param pbstrName [out]

Pointer to a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a> variable that, on successful return, receives the name of the connection.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnectionprops">INetConnectionProps</a>
 

 

