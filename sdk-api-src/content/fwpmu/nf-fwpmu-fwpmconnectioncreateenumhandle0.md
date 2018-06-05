---
UID: NF:fwpmu.FwpmConnectionCreateEnumHandle0
title: FwpmConnectionCreateEnumHandle0 function
author: windows-sdk-content
description: Creates a handle used to enumerate a set of connection objects.
old-location: fwp\fwpmconnectioncreateenumhandle0.htm
old-project: FWP
ms.assetid: b33878d5-437d-4625-b488-28fbe95eb69f
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmConnectionCreateEnumHandle0, FwpmConnectionCreateEnumHandle0 function [Filtering], fwp.fwpmconnectioncreateenumhandle0, fwpmu/FwpmConnectionCreateEnumHandle0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmConnectionCreateEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmConnectionCreateEnumHandle0 function


## -description


The <b>FwpmConnectionCreateEnumHandle0</b> function creates a handle used to enumerate a set of connection objects.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/1939e4ae-9ff8-4ee7-895b-2ed992204b5c">FWPM_CONNECTION_ENUM_TEMPLATE0</a>*</b>

Template for selectively restricting the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

Address of a <b>HANDLE</b> variable. On function return, it contains the handle for the enumeration.


## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The enumerator was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



If <i>enumTemplate</i> is <b>NULL</b>, all connection objects are returned.

The caller must free the returned handle by a call to <a href="https://msdn.microsoft.com/0325908e-4d2b-4cdb-9cfa-f2985a76dba9">FwpmConnectionDestroyEnumHandle0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ENUM</a> access to the connection objects' containers and <b>FWPM_ACTRL_READ</b> access to the connection objects. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/1939e4ae-9ff8-4ee7-895b-2ed992204b5c">FWPM_CONNECTION_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/0325908e-4d2b-4cdb-9cfa-f2985a76dba9">FwpmConnectionDestroyEnumHandle0</a>
 

 

