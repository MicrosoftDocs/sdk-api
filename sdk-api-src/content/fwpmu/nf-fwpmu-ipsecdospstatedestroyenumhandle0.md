---
UID: NF:fwpmu.IPsecDospStateDestroyEnumHandle0
title: IPsecDospStateDestroyEnumHandle0 function
author: windows-sdk-content
description: Frees a handle returned by IPsecDospStateCreateEnumHandle0.
old-location: fwp\ipsecdospstatedestroyenumhandle0.htm
tech.root: fwp
ms.assetid: d7e1710d-8142-4583-a7b6-960fbdb2fcbb
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPsecDospStateDestroyEnumHandle0, IPsecDospStateDestroyEnumHandle0 function [Filtering], fwp.ipsecdospstatedestroyenumhandle0, fwpmu/IPsecDospStateDestroyEnumHandle0
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
 - IPsecDospStateDestroyEnumHandle0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IPsecDospStateDestroyEnumHandle0
: 
---

# IPsecDospStateDestroyEnumHandle0 function


## -description


The <b>IPsecDospStateDestroyEnumHandle0</b> function frees a handle returned by <a href="https://msdn.microsoft.com/5ceb78eb-bcbf-48fe-b2a9-52a687e5ce20">IPsecDospStateCreateEnumHandle0</a>.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in, out]

Type: <b>HANDLE</b>

Handle of the enumeration to destroy. Previously created by a call to <a href="https://msdn.microsoft.com/5ceb78eb-bcbf-48fe-b2a9-52a687e5ce20">IPsecDospStateCreateEnumHandle0</a>.


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
The enumeration was deleted successfully.

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



<b>IPsecDospStateDestroyEnumHandle0</b> is a specific implementation of IPsecDospStateDestroyEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/5ceb78eb-bcbf-48fe-b2a9-52a687e5ce20">IPsecDospStateCreateEnumHandle0</a>
 

 

