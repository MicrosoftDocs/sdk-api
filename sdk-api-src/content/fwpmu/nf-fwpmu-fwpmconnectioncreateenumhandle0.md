---
UID: NF:fwpmu.FwpmConnectionCreateEnumHandle0
title: FwpmConnectionCreateEnumHandle0 function (fwpmu.h)
description: Creates a handle used to enumerate a set of connection objects.helpviewer_keywords: ["FwpmConnectionCreateEnumHandle0","FwpmConnectionCreateEnumHandle0 function [Filtering]","fwp.fwpmconnectioncreateenumhandle0","fwpmu/FwpmConnectionCreateEnumHandle0"]
old-location: fwp\fwpmconnectioncreateenumhandle0.htm
tech.root: fwp
ms.assetid: b33878d5-437d-4625-b488-28fbe95eb69f
ms.date: 12/05/2018
ms.keywords: FwpmConnectionCreateEnumHandle0, FwpmConnectionCreateEnumHandle0 function [Filtering], fwp.fwpmconnectioncreateenumhandle0, fwpmu/FwpmConnectionCreateEnumHandle0
f1_keywords:
- fwpmu/FwpmConnectionCreateEnumHandle0
dev_langs:
- c++
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Fwpuclnt.dll
api_name:
- FwpmConnectionCreateEnumHandle0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmConnectionCreateEnumHandle0 function


## -description


The <b>FwpmConnectionCreateEnumHandle0</b> function creates a handle used to enumerate a set of connection objects.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: [FWPM_CONNECTION_ENUM_TEMPLATE0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)a>*</b>

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
A Windows Filtering Platform (WFP) specific error. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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

The caller must free the returned handle by a call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0">FwpmConnectionDestroyEnumHandle0</a>.

The caller needs <a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ENUM</a> access to the connection objects' containers and <b>FWPM_ACTRL_READ</b> access to the connection objects. See <a href="https://docs.microsoft.com/windows/desktop/FWP/access-control">Access Control</a> for more information.




## -see-also




[FWPM_CONNECTION_ENUM_TEMPLATE0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0">FwpmConnectionDestroyEnumHandle0</a>
 

 

