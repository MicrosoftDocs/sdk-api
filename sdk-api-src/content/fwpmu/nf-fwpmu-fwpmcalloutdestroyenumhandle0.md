---
UID: NF:fwpmu.FwpmCalloutDestroyEnumHandle0
title: FwpmCalloutDestroyEnumHandle0 function
author: windows-sdk-content
description: Frees a handle returned by FwpmCalloutCreateEnumHandle0.
old-location: fwp\fwpmcalloutdestroyenumhandle0_func.htm
tech.root: fwp
ms.assetid: 6aa41eed-b53c-4b35-a45c-88f89086cacc
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FwpmCalloutDestroyEnumHandle0, FwpmCalloutDestroyEnumHandle0 function [Filtering], fwp.fwpmcalloutdestroyenumhandle0_func, fwpmu/FwpmCalloutDestroyEnumHandle0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
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
 - FwpmCalloutDestroyEnumHandle0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmCalloutDestroyEnumHandle0 function


## -description


The <b>FwpmCalloutDestroyEnumHandle0</b> function frees a handle returned by <a href="https://msdn.microsoft.com/bd37eebb-8a07-4b67-9595-34cc96463254">FwpmCalloutCreateEnumHandle0</a>.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle of a callout enumeration created by a call to <a href="https://msdn.microsoft.com/bd37eebb-8a07-4b67-9595-34cc96463254">FwpmCalloutCreateEnumHandle0</a>.


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
The enumerator was successfully deleted.

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



<b>FwpmCalloutDestroyEnumHandle0</b> is a specific implementation of FwpmCalloutDestroyEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/bd37eebb-8a07-4b67-9595-34cc96463254">FwpmCalloutCreateEnumHandle0</a>
 

 

