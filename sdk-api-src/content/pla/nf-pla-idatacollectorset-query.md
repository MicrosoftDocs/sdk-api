---
UID: NF:pla.IDataCollectorSet.Query
title: IDataCollectorSet::Query (pla.h)
description: Retrieves the specified data collector set.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Query method","IDataCollectorSet.Query","IDataCollectorSet::Query","Query","Query method [PLA]","Query method [PLA]","IDataCollectorSet interface","base.idatacollectorset_query","pla.idatacollectorset_query","pla/IDataCollectorSet::Query"]
old-location: pla\idatacollectorset_query.htm
tech.root: PLA
ms.assetid: ac07169e-710c-4267-ae08-ed18a15d866d
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Query method, IDataCollectorSet.Query, IDataCollectorSet::Query, Query, Query method [PLA], Query method [PLA],IDataCollectorSet interface, base.idatacollectorset_query, pla.idatacollectorset_query, pla/IDataCollectorSet::Query
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollectorSet::Query
 - pla/IDataCollectorSet::Query
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.Query
---

# IDataCollectorSet::Query


## -description

Retrieves the specified data collector set.

## -parameters

### -param name [in]

The name of the data collector set to retrieve. The name is case-insensitive and is of the form <b>[</b><i>Namespace</i><b>\]</b><i>Name</i>. For details on the optional namespace, see Remarks.

### -param server [in]

The computer on which the set exists. You can specify a computer name, a fully qualified domain name, or an IP address (IPv4 or IPv6 format). If <b>NULL</b>, the set is retrieved from the local computer.

## -returns

Returns S_OK if successful. The following table shows possible error values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLA_E_DCS_NOT_FOUND</b></dt>
<dt>0x80300002</dt>
</dl>
</td>
<td width="60%">
The specified data collector set was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
<dt>0x80300002</dt>
</dl>
</td>
<td width="60%">
You must retrieve a data collector set into an empty instance or into an instance that uses the same namespace.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)</b></dt>
</dl>
</td>
<td width="60%">
The RPC server is not available. The method is unable to query the data collector set remotely. To query the data collector set from a remote computer running Windows Vista, enable Performance Logs and Alerts in <b>Windows Firewall Settings</b> on the remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BAD_NETPATH)</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the remote computer.

</td>
</tr>
</table>

## -remarks

The contents of the retrieved data collector set overwrites the contents of this instance. The instance must be empty (newly created) or be from the same namespace.

Specify the same <i>name</i> and <i>server</i> parameter values that you specified when calling the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a> method to save the set.

The <i>name</i> parameter can contain an optional namespace; however, you should always specify the namespace. If you do not specify the namespace, PLA uses "Service" for computers running Windows Vista and "Legacy" for computers running operating systems prior to Windows Vista. The following table lists the possible namespace values. 

<table>
<tr>
<th>Namespace</th>
<th>Description</th>
</tr>
<tr>
<td>
Autosession

</td>
<td>
Contains ETW <a href="/windows/desktop/ETW/configuring-and-starting-an-autologger-session">AutoLogger</a> sessions. The collector starts when the computer starts, cannot be stopped, and the status is undefined.

</td>
</tr>
<tr>
<td>
Legacy

</td>
<td>
Same as Service but on computers running an operating system that is prior to Windows Vista.

</td>
</tr>
<tr>
<td>
Service

</td>
<td>
Contains all data collector sets created by the user. These sets can be scheduled and can be set to run as anyone (the user needs the batch logon account right). If you do not specify credentials, the set will run as LocalSystem (if the user is an administrator).

</td>
</tr>
<tr>
<td>
Session

</td>
<td>
Contains <a href="/windows/desktop/ETW/event-tracing-portal">Event Tracing for Windows</a> (ETW) trace sessions. These sets cannot be scheduled. If you use this namespace, the set must contain only one data collector and it must be a trace data collector.

</td>
</tr>
<tr>
<td>
System

</td>
<td>
Contains read-only data collector sets that cannot be scheduled; however, you can start these sets manually. If you do not specify credentials, the set will run as the current user.

</td>
</tr>
</table>
 

Note that the Service namespace can be used in place of the Legacy namespace on computers running operating systems prior to Windows Vista.

To query all committed sets on a computer, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorsetcollection-getdatacollectorsets">IDataCollectorSetCollection::GetDataCollectorSets</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-delete">IDataCollectorSet::Delete</a>