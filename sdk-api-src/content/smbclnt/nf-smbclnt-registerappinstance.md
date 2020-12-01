---
UID: NF:smbclnt.RegisterAppInstance
title: RegisterAppInstance function (smbclnt.h)
description: Registers the AppInstance ID for a process.
helpviewer_keywords: ["PREGISTER_APPINSTANCE","PREGISTER_APPINSTANCE function [Failover Cluster]","RegisterAppInstance","RegisterAppInstance function [Failover Cluster]","mscs.registerappinstance","smbclnt/PREGISTER_APPINSTANCE","smbclnt/RegisterAppInstance"]
old-location: mscs\registerappinstance.htm
tech.root: MsCS
ms.assetid: 43CAC59A-5773-44BD-8965-F9FB85B86926
ms.date: 12/05/2018
ms.keywords: PREGISTER_APPINSTANCE, PREGISTER_APPINSTANCE function [Failover Cluster], RegisterAppInstance, RegisterAppInstance function [Failover Cluster], mscs.registerappinstance, smbclnt/PREGISTER_APPINSTANCE, smbclnt/RegisterAppInstance
req.header: smbclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NTLanMan.lib
req.dll: NTLanMan.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterAppInstance
 - smbclnt/RegisterAppInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NTLanMan.dll
api_name:
 - RegisterAppInstance
---

# RegisterAppInstance function


## -description

Registers the <i>AppInstance</i> ID for a process.

## -parameters

### -param ProcessHandle [in]

A process handle for the current process or a remote process to be tagged with the 
      <i>AppInstanceId</i>. To tag a remote process, the handle must have 
      <b>PROCESS_TERMINATE</b> access to that process.

### -param AppInstanceId [in]

The application instance ID, which is a <b>GUID</b>.

### -param ChildrenInheritAppInstance [in]

<b>TRUE</b> to tag the child processes spawned by the process specified by 
       <i>ProcessHandle</i>; otherwise, <b>FALSE</b>.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The CCF Filter failed to allocate the proper cache objects to fulfill this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The current process that's trying to tag the process specified by 
        <i>ProcessHandle</i> doesn't have <b>PROCESS_TERMINATE</b> 
        access to that process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>ProcessHandle</i> is not a handle to a process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The CCF mini-filter is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Another <i>AppInstance</i><b>GUID</b> is provided for the same 
        process, which means that the 
        <a href="/windows/desktop/api/smbclnt/nf-smbclnt-registerappinstance">RegisterAppInstance</a> function was called twice 
        or the application was registered twice.

</td>
</tr>
</table>

## -remarks

The <b>RegisterAppInstance</b> function issues an 
     <b>IOCTL_CCF_REGISTER_APPINSTANCE</b> call to the CCF mini-filter. The function 
     passes the <i>AppInstance</i> <b>GUID</b>, the 
     process handle, and the tagged child processes to the CCF cache that maps the process handle to the 
     <i>AppInstanceId</i>.

The issued IOCTL for tagging another process checks if the current process has 
     <b>PROCESS_TERMINATE</b> access to the target process.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>