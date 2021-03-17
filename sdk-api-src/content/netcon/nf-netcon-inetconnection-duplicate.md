---
UID: NF:netcon.INetConnection.Duplicate
title: INetConnection::Duplicate (netcon.h)
description: The Duplicate method creates a duplicate of this connection in the connections folder.
helpviewer_keywords: ["Duplicate","Duplicate method [ICS/ICF]","Duplicate method [ICS/ICF]","INetConnection interface","INetConnection interface [ICS/ICF]","Duplicate method","INetConnection.Duplicate","INetConnection::Duplicate","_ics_inetconnection_duplicate","ics.inetconnection_duplicate","netcon/INetConnection::Duplicate"]
old-location: ics\inetconnection_duplicate.htm
tech.root: ics
ms.assetid: 1196e66d-95c1-4417-ac0d-b84583879d6a
ms.date: 12/05/2018
ms.keywords: Duplicate, Duplicate method [ICS/ICF], Duplicate method [ICS/ICF],INetConnection interface, INetConnection interface [ICS/ICF],Duplicate method, INetConnection.Duplicate, INetConnection::Duplicate, _ics_inetconnection_duplicate, ics.inetconnection_duplicate, netcon/INetConnection::Duplicate
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
 - INetConnection::Duplicate
 - netcon/INetConnection::Duplicate
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
 - INetConnection.Duplicate
---

# INetConnection::Duplicate


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>Duplicate</b> method creates a duplicate of this connection in the connections folder.

## -parameters

### -param pszwDuplicateName [in]

Pointer to a Unicode string that specifies the name for the new connection.

### -param ppCon [out]

Pointer to an interface pointer that, on successful return, points to an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a> interface for the new connection.

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

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>