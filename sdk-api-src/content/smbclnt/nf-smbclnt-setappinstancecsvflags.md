---
UID: NF:smbclnt.SetAppInstanceCsvFlags
title: SetAppInstanceCsvFlags function (smbclnt.h)
description: Sets the flags that affect connections from the application instance.
helpviewer_keywords: ["SET_APP_INSTANCE_CSV_FLAGS","SET_APP_INSTANCE_CSV_FLAGS function [Failover Cluster]","SetAppInstanceCsvFlags","SetAppInstanceCsvFlags function [Failover Cluster]","mscs.setappinstancecsvflags","smbclnt/SET_APP_INSTANCE_CSV_FLAGS","smbclnt/SetAppInstanceCsvFlags"]
old-location: mscs\setappinstancecsvflags.htm
tech.root: MsCS
ms.assetid: 37FDAB0A-1593-47D6-B4CE-A667EBA01680
ms.date: 12/05/2018
ms.keywords: SET_APP_INSTANCE_CSV_FLAGS, SET_APP_INSTANCE_CSV_FLAGS function [Failover Cluster], SetAppInstanceCsvFlags, SetAppInstanceCsvFlags function [Failover Cluster], mscs.setappinstancecsvflags, smbclnt/SET_APP_INSTANCE_CSV_FLAGS, smbclnt/SetAppInstanceCsvFlags
req.header: smbclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - SetAppInstanceCsvFlags
 - smbclnt/SetAppInstanceCsvFlags
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
 - SetAppInstanceCsvFlags
---

# SetAppInstanceCsvFlags function


## -description

Sets the flags that affect connections from the application instance.

## -parameters

### -param ProcessHandle [in]

A process handle for the current process or a remote process to be tagged with the 
      application instance. To tag a remote process, the handle must have 
      <b>PROCESS_TERMINATE</b> access to that process.

### -param Mask [in]

A bitmask that indicates the flags that are modified by the <i>Flags</i> parameter.

### -param Flags [in]

New values of the flags.

## -returns

Returns "0" if the operation is successful; otherwise, one of the following error codes is returned:

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
The CCF filter failed to allocate the                  cache objects for the operation.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The CCF mini-filter was                  not found.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>