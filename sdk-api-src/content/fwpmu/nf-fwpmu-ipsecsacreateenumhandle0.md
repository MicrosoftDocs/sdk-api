---
UID: NF:fwpmu.IPsecSaCreateEnumHandle0
title: IPsecSaCreateEnumHandle0 function
author: windows-sdk-content
description: Creates a handle used to enumerate a set of Internet Protocol Security (IPsec) security association (SA) objects.
old-location: fwp\ipsecsacreateenumhandle0_func.htm
tech.root: FWP
ms.assetid: 473935d9-362f-417c-a366-f683d97d9a18
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IPsecSaCreateEnumHandle0, IPsecSaCreateEnumHandle0 function [Filtering], fwp.ipsecsacreateenumhandle0_func, fwpmu/IPsecSaCreateEnumHandle0
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
 - IPsecSaCreateEnumHandle0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecSaCreateEnumHandle0 function


## -description


The <b>IPsecSaCreateEnumHandle0</b> function creates a handle used to enumerate a set of Internet Protocol Security (IPsec) security association (SA) objects.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/6a00af2b-0b39-4d9f-9335-4817df693b52">IPSEC_SA_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle of the newly created enumeration.


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
The enumeration was created successfully.

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



If <i>enumTemplate</i> is <b>NULL</b>, all IPsec SA objects are returned.

The caller must call <a href="https://msdn.microsoft.com/acd02e35-0bcb-4882-9b85-b29a558d34b7">IPsecSaDestroyEnumHandle0</a> to free the returned handle.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> and <b>FWPM_ACTRL_ENUM</b> access to the IPsec security associations database. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>IPsecSaCreateEnumHandle0</b> is a specific implementation of IPsecSaCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/6a00af2b-0b39-4d9f-9335-4817df693b52">IPSEC_SA_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/acd02e35-0bcb-4882-9b85-b29a558d34b7">IPsecSaDestroyEnumHandle0</a>
 

 

