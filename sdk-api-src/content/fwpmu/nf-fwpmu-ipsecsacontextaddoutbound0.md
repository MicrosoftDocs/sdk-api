---
UID: NF:fwpmu.IPsecSaContextAddOutbound0
title: IPsecSaContextAddOutbound0 function
author: windows-sdk-content
description: The IPsecSaContextAddOutbound0 function adds an outbound IPsec security association (SA) bundle to an existing SA context.Note  IPsecSaContextAddOutbound0 is the specific implementation of IPsecSaContextAddOutbound used in Windows Vista.
old-location: fwp\ipsecsacontextaddoutbound0.htm
tech.root: fwp
ms.assetid: f7aa0b1f-160c-44d4-9dbc-5c692d0a4467
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPsecSaContextAddOutbound0, IPsecSaContextAddOutbound0 function [Filtering], fwp.ipsecsacontextaddoutbound0, fwpmu/IPsecSaContextAddOutbound0
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
 - IPsecSaContextAddOutbound0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IPsecSaContextAddOutbound0
: 
---

# IPsecSaContextAddOutbound0 function


## -description


The <b>IPsecSaContextAddOutbound0</b> function adds an outbound IPsec security association (SA) bundle to an existing SA context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextAddOutbound0</b> is the specific implementation of IPsecSaContextAddOutbound used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/ca8bc833-4d6f-4ed0-9c9b-15bbca5e0090">IPsecSaContextAddOutbound1</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

Identifier for the existing IPsec SA context. This is the value returned in the <i>id</i> parameter by the call to  <a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a>.


### -param outboundBundle [in]

Type: <b>const <a href="https://msdn.microsoft.com/65376dd9-e06c-41ff-8689-74be12c47239">IPSEC_SA_BUNDLE0</a>*</b>

The outbound IPsec SA bundle to be added to the SA context.


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
The IPsec SA bundle was successfully added to the SA context.

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
 




## -see-also




<a href="https://msdn.microsoft.com/65376dd9-e06c-41ff-8689-74be12c47239">IPSEC_SA_BUNDLE0</a>



<a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a>
 

 

