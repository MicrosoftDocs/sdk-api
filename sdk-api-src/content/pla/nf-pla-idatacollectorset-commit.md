---
UID: NF:pla.IDataCollectorSet.Commit
title: IDataCollectorSet::Commit (pla.h)
description: Saves, updates, or validates the data collector set. You can also use this method to flush a trace session.
helpviewer_keywords: ["Commit","Commit method [PLA]","Commit method [PLA]","IDataCollectorSet interface","IDataCollectorSet interface [PLA]","Commit method","IDataCollectorSet.Commit","IDataCollectorSet::Commit","base.idatacollectorset_commit","pla.idatacollectorset_commit","pla/IDataCollectorSet::Commit"]
old-location: pla\idatacollectorset_commit.htm
tech.root: PLA
ms.assetid: 7e432e1f-4b86-45dc-93d5-df603068273d
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [PLA], Commit method [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],Commit method, IDataCollectorSet.Commit, IDataCollectorSet::Commit, base.idatacollectorset_commit, pla.idatacollectorset_commit, pla/IDataCollectorSet::Commit
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
 - IDataCollectorSet::Commit
 - pla/IDataCollectorSet::Commit
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
 - IDataCollectorSet.Commit
---

# IDataCollectorSet::Commit


## -description

Saves, updates, or validates the data collector set. You can also use this method to flush a trace session.

## -parameters

### -param name [in]

A unique name used to save the data collector set. The name is of the form  <b>[</b><i>Namespace</i><b>\]</b><i>Name</i>. For details, see Remarks.

### -param server [in]

The computer on which you want to save the set. You can specify a computer name, a fully qualified domain name, or an IP address (IPv4 or IPv6 format). If <b>NULL</b>, the set is saved to the local computer.

### -param mode [in]

Indicates whether you want to save, update, flush, or validate the data collector set. For possible values, see the <a href="/windows/win32/api/pla/ne-pla-commitmode">CommitMode</a> enumeration.

### -param validation [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid or is ignored. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_count">IValueMap::Count</a> property is zero if there were no errors or warnings.

## -returns

Returns S_OK if the method call was successful. You must check the value map for errors (see Remarks). If the method returns S_OK	and there are no validation errors, then the set was successfully committed. The following table shows possible error values when calling this method.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The user must be running as an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The specified namespace is not supported (for example, if you specified the System namespace when committing the data collector set on a computer running an operating system prior to Windows Vista).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)</b></dt>
</dl>
</td>
<td width="60%">
The RPC server is not available. The method is unable to save the data collector set remotely. To commit remotely to a computer running Windows Vista, enable Performance Logs and Alerts in <b>Windows Firewall Settings</b> on the remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLA_E_DCS_ALREADY_EXISTS</b></dt>
<dt>0x803000B7</dt>
</dl>
</td>
<td width="60%">
You are trying to commit a new set, but a set with the specified name already exists.

</td>
</tr>
</table>

## -remarks

If you save the set, use the specified <i>name</i> and <i>server</i> parameter values when calling the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-query">IDataCollectorSet::Query</a> method to retrieve the set.

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
Contains all data collector sets created by the user. These sets can be scheduled and can be set to run as anyone. The user needs the <b>Log on as a batch job</b> account right (see Administrative Tools, Local Security Policy, Local Policies, User Rights Assignment). If you do not specify credentials, the set will run as LocalSystem (if the user is an administrator).

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

To determine the validation errors that occurred, retrieve the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface for each error in the value map collection. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the XPath of the element in error, for example, /AlertDataCollector/TaskArguments. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the HRESULT value, which can be an error or warning (success code). The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_description">IValueMapItem::Description</a> property contains the message text associated with the error.

Typically, any errors that occur will be one of the following HRESULT values in the value map collection.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>
PLA_S_PROPERTY_IGNORED

</td>
<td>
The property is not used. PLA uses this warning to disable the item in its UI so the user knows the property is being ignored.

</td>
</tr>
<tr>
<td>
PLA_E_PROPERTY_CONFLICT

</td>
<td>
The property conflicts with another property, for example, both <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logappend">LogAppend</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logcircular">LogCircular</a> are <b>VARIANT_TRUE</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-delete">IDataCollectorSet::Delete</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-query">IDataCollectorSet::Query</a>