---
UID: NF:fwpmu.IPsecDospStateCreateEnumHandle0
title: IPsecDospStateCreateEnumHandle0 function (fwpmu.h)
author: windows-sdk-content
description: Creates a handle used to enumerate a set of IPsec DoS Protection objects.
old-location: fwp\ipsecdospstatecreateenumhandle0.htm
tech.root: fwp
ms.assetid: 5ceb78eb-bcbf-48fe-b2a9-52a687e5ce20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPsecDospStateCreateEnumHandle0, IPsecDospStateCreateEnumHandle0 function [Filtering], fwp.ipsecdospstatecreateenumhandle0, fwpmu/IPsecDospStateCreateEnumHandle0
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
 - IPsecDospStateCreateEnumHandle0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecDospStateCreateEnumHandle0 function


## -description


The <b>IPsecDospStateCreateEnumHandle0</b> function creates a handle used to enumerate a set of IPsec DoS Protection objects.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dd744996(v=VS.85).aspx">IPSEC_DOSP_STATE_ENUM_TEMPLATE0</a>*</b>

Template for selectively restricting the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

Address of a <b>HANDLE</b> variable. On function return, it contains the handle for the newly created enumeration.




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



If <i>enumTemplate</i> is <b>NULL</b>, all IPsec DoS Protection objects are returned.

The caller must call <a href="https://msdn.microsoft.com/d7e1710d-8142-4583-a7b6-960fbdb2fcbb">IPsecDospStateDestroyEnumHandle0</a> to free the returned handle.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ_STATS</a> access to the IPsec DoS Protection component. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>IPsecDospStateCreateEnumHandle0</b> is a specific implementation of IPsecDospStateCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd744996(v=VS.85).aspx">IPSEC_DOSP_STATE_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/d7e1710d-8142-4583-a7b6-960fbdb2fcbb">IPsecDospStateDestroyEnumHandle0</a>
 

 

