---
UID: NF:netcon.IEnumNetSharingEveryConnection.Reset
title: IEnumNetSharingEveryConnection::Reset (netcon.h)
description: The Reset method causes subsequent enumeration calls to operate from the beginning of the enumeration.
helpviewer_keywords: ["IEnumNetSharingEveryConnection interface [ICS/ICF]","Reset method","IEnumNetSharingEveryConnection.Reset","IEnumNetSharingEveryConnection::Reset","Reset","Reset method [ICS/ICF]","Reset method [ICS/ICF]","IEnumNetSharingEveryConnection interface","_ics_ienumnetsharingeveryconnection_reset","ics.ienumnetsharingeveryconnection_reset","netcon/IEnumNetSharingEveryConnection::Reset"]
old-location: ics\ienumnetsharingeveryconnection_reset.htm
tech.root: ics
ms.assetid: c41539b9-2596-4bb4-9194-fa9accde165d
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingEveryConnection interface [ICS/ICF],Reset method, IEnumNetSharingEveryConnection.Reset, IEnumNetSharingEveryConnection::Reset, Reset, Reset method [ICS/ICF], Reset method [ICS/ICF],IEnumNetSharingEveryConnection interface, _ics_ienumnetsharingeveryconnection_reset, ics.ienumnetsharingeveryconnection_reset, netcon/IEnumNetSharingEveryConnection::Reset
f1_keywords:
- netcon/IEnumNetSharingEveryConnection.Reset
dev_langs:
- c++
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
- IEnumNetSharingEveryConnection.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumNetSharingEveryConnection::Reset


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>Reset</b> method causes subsequent enumeration calls to operate from the beginning of the enumeration.


## -parameters






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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-ienumnetsharingeveryconnection">IEnumNetSharingEveryConnection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

