---
UID: NF:fwpmu.IPsecSaContextAddInbound1
title: IPsecSaContextAddInbound1 function
author: windows-sdk-content
description: The IPsecSaContextAddInbound1 function adds an inbound IPsec security association (SA) bundle to an existing SA context.Note  IPsecSaContextAddInbound1 is the specific implementation of IPsecSaContextAddInbound used in Windows 7 and later.
old-location: fwp\ipsecsacontextaddinbound1.htm
tech.root: FWP
ms.assetid: a6717ff9-41f9-4cbc-9493-b9d80a137571
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPsecSaContextAddInbound1, IPsecSaContextAddInbound1 function [Filtering], fwp.ipsecsacontextaddinbound1, fwpmu/IPsecSaContextAddInbound1
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPsecSaContextAddInbound1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecSaContextAddInbound1 function


## -description


The <b>IPsecSaContextAddInbound1</b> function adds an inbound IPsec security association (SA) bundle to an existing SA context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextAddInbound1</b> is the specific implementation of IPsecSaContextAddInbound used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/e0798bcb-847d-481e-b9f0-b18c0bbad22c">IPsecSaContextAddInbound0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

Identifier for the existing IPsec SA context. This is the value returned in the <i>id</i> parameter by the call to  <a href="https://msdn.microsoft.com/b0eab185-fae2-4133-b3f2-22d609cb94d1">IPsecSaContextCreate1</a>.


### -param inboundBundle [in]

Type: <b>const <a href="https://msdn.microsoft.com/491f43ca-07ce-460f-8c20-e5eb0f7bcac4">IPSEC_SA_BUNDLE1</a>*</b>

The inbound IPsec SA bundle to be added to the SA context.


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




<a href="https://msdn.microsoft.com/491f43ca-07ce-460f-8c20-e5eb0f7bcac4">IPSEC_SA_BUNDLE1</a>



<a href="https://msdn.microsoft.com/b0eab185-fae2-4133-b3f2-22d609cb94d1">IPsecSaContextCreate1</a>
 

 

