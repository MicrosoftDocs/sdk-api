---
UID: NF:netcon.IEnumNetSharingPublicConnection.Reset
title: IEnumNetSharingPublicConnection::Reset (netcon.h)
description: The Reset method causes subsequent enumeration calls to operate from the beginning of the enumeration. (IEnumNetSharingPublicConnection.Reset)
helpviewer_keywords: ["IEnumNetSharingPublicConnection interface [ICS/ICF]","Reset method","IEnumNetSharingPublicConnection.Reset","IEnumNetSharingPublicConnection::Reset","Reset","Reset method [ICS/ICF]","Reset method [ICS/ICF]","IEnumNetSharingPublicConnection interface","_ics_ienumnetsharingpublicconnection_reset","ics.ienumnetsharingpublicconnection_reset","netcon/IEnumNetSharingPublicConnection::Reset"]
old-location: ics\ienumnetsharingpublicconnection_reset.htm
tech.root: ics
ms.assetid: f58a9efb-bb0d-477c-946f-5bef6c5635d8
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingPublicConnection interface [ICS/ICF],Reset method, IEnumNetSharingPublicConnection.Reset, IEnumNetSharingPublicConnection::Reset, Reset, Reset method [ICS/ICF], Reset method [ICS/ICF],IEnumNetSharingPublicConnection interface, _ics_ienumnetsharingpublicconnection_reset, ics.ienumnetsharingpublicconnection_reset, netcon/IEnumNetSharingPublicConnection::Reset
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumNetSharingPublicConnection::Reset
 - netcon/IEnumNetSharingPublicConnection::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - IEnumNetSharingPublicConnection.Reset
---

# IEnumNetSharingPublicConnection::Reset


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>Reset</b> method causes subsequent enumeration calls to operate from the beginning of the enumeration.



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

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-ienumnetsharingpublicconnection">IEnumNetSharingPublicConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
