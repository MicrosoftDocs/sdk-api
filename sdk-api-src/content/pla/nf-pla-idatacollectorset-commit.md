---
UID: NF:pla.IDataCollectorSet.Commit
title: IDataCollectorSet::Commit
author: windows-sdk-content
description: Saves, updates, or validates the data collector set. You can also use this method to flush a trace session.
old-location: pla\idatacollectorset_commit.htm
old-project: PLA
ms.assetid: 7e432e1f-4b86-45dc-93d5-df603068273d
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Commit, Commit method [PLA], Commit method [PLA],IDataCollectorSet interface, IDataCollectorSet interface [PLA],Commit method, IDataCollectorSet.Commit, IDataCollectorSet::Commit, base.idatacollectorset_commit, pla.idatacollectorset_commit, pla/IDataCollectorSet::Commit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.Commit
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: ADAM
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

Indicates whether you want to save, update, flush, or validate the data collector set. For possible values, see the <a href="https://msdn.microsoft.com/3c485b4d-ba0b-456a-b942-27829371d7fb">CommitMode</a> enumeration.


### -param validation [out]

An <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface that you use to retrieve the validation error of each property whose value is not valid or is ignored. The <a href="https://msdn.microsoft.com/990b48d8-357f-4157-a3d2-1ea1c80e1887">IValueMap::Count</a> property is zero if there were no errors or warnings.


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



If you save the set, use the specified <i>name</i> and <i>server</i> parameter values when calling the <a href="https://msdn.microsoft.com/ac07169e-710c-4267-ae08-ed18a15d866d">IDataCollectorSet::Query</a> method to retrieve the set.

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
Contains ETW <a href="https://msdn.microsoft.com/df5a79f4-abbf-4b83-afc3-cbd14b166067">AutoLogger</a> sessions. The collector starts when the computer starts, cannot be stopped, and the status is undefined.

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
Contains <a href="https://msdn.microsoft.com/library/windows/hardware/dn938554">Event Tracing for Windows</a> (ETW) trace sessions. These sets cannot be scheduled. If you use this namespace, the set must contain only one data collector and it must be a trace data collector.

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

To determine the validation errors that occurred, retrieve the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface for each error in the value map collection. The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the XPath of the element in error, for example, /AlertDataCollector/TaskArguments. The <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the HRESULT value, which can be an error or warning (success code). The <a href="https://msdn.microsoft.com/ee0669f1-6400-4c32-9f5f-82fd69b7cacd">IValueMapItem::Description</a> property contains the message text associated with the error.

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
The property conflicts with another property, for example, both <a href="https://msdn.microsoft.com/c9843647-2c36-4d08-98d0-4df63b054993">LogAppend</a> and <a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">LogCircular</a> are <b>VARIANT_TRUE</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/35e95d41-0d6c-428a-a167-6667275d4fb7">IDataCollectorSet::Delete</a>



<a href="https://msdn.microsoft.com/ac07169e-710c-4267-ae08-ed18a15d866d">IDataCollectorSet::Query</a>
 

 

