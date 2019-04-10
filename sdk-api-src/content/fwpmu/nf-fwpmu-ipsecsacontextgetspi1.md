---
UID: NF:fwpmu.IPsecSaContextGetSpi1
title: IPsecSaContextGetSpi1 function (fwpmu.h)
author: windows-sdk-content
description: Retrieves the security parameters index (SPI) for a security association (SA) context.
old-location: fwp\ipsecsacontextgetspi1.htm
tech.root: fwp
ms.assetid: 623ef4ab-5bcc-4801-ba18-a246da392abe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPsecSaContextGetSpi1, IPsecSaContextGetSpi1 function [Filtering], fwp.ipsecsacontextgetspi1, fwpmu/IPsecSaContextGetSpi1
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
 - IPsecSaContextGetSpi1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecSaContextGetSpi1 function


## -description


The <b>IPsecSaContextGetSpi1</b> function retrieves the security parameters index (SPI) for a security association (SA) context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextGetSpi1</b> is the specific implementation of IPsecSaContextGetSpi used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/dac82051-db36-450a-a59a-61df6bad6694">IPsecSaContextGetSpi0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

A runtime identifier for the SA context. This identifier was received from the system when the application called <a href="https://msdn.microsoft.com/b0eab185-fae2-4133-b3f2-22d609cb94d1">IPsecSaContextCreate1</a>.


### -param getSpi [in]

Type: <b>const <a href="https://msdn.microsoft.com/671a8dd2-b4f6-4bdd-a6f1-1bf4260c6cbe">IPSEC_GETSPI1</a>*</b>

The inbound IPsec traffic.


### -param inboundSpi [out]

Type: <b>IPSEC_SA_SPI*</b>

The inbound SA SPI. The <b>IPSEC_SA_SPI</b> data type maps to the <b>UINT32</b> data type.


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
The SPI for the IPsec SA context was retrieved successfully.

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



The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ADD</a> access to the IPsec security associations database. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/671a8dd2-b4f6-4bdd-a6f1-1bf4260c6cbe">IPSEC_GETSPI1</a>



<a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a>
 

 

