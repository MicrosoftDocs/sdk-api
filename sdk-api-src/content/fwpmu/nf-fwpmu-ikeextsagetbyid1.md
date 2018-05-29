---
UID: NF:fwpmu.IkeextSaGetById1
title: IkeextSaGetById1 function
author: windows-sdk-content
description: Retrieves an IKE/AuthIP security association (SA) from the database.
old-location: fwp\ikeextsagetbyid1.htm
old-project: FWP
ms.assetid: 99861d5e-31df-47ef-a922-a1720b17c70e
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IkeextSaGetById1, IkeextSaGetById1 function [Filtering], fwp.ikeextsagetbyid1, fwpmu/IkeextSaGetById1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	IkeextSaGetById1
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# IkeextSaGetById1 function


## -description


The <b>IkeextSaGetById1</b> function retrieves an IKE/AuthIP security association (SA) from the database. 
<div class="alert"><b>Note</b>  <b>IkeextSaGetById1</b> is the specific implementation of IkeextSaGetById used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/5ea04fdc-d06d-4e8e-9c66-3a6df4372481">IkeextSaGetById2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/c500f7d1-ce8f-4a4e-9f09-c37116ef9ab3">IkeextSaGetById0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

The SA identifier.


### -param saLookupContext [in, optional]

Type: <b>GUID*</b>

Optional pointer to the SA lookup context propagated from the SA to data connections flowing over that SA. It is made available to any application that queries socket security properties using the Winsock API <a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a> function, allowing the application to obtain detailed IPsec authentication information for its connection.


### -param sa [out]

Type: <b><a href="https://msdn.microsoft.com/b4b8767b-399a-49f0-91fd-59c2206742de">IKEEXT_SA_DETAILS1</a>**</b>

Address of the SA details.


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
The SA was retrieved successfully.

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



The caller must free <i>sa</i> by a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the IKE/AuthIP security associations database. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/df36b6cc-a304-4426-8f16-1bf92fd721e1">IKE/AuthIP Functions</a>



<a href="https://msdn.microsoft.com/b4b8767b-399a-49f0-91fd-59c2206742de">IKEEXT_SA_DETAILS1</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

