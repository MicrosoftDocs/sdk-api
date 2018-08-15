---
UID: NF:fwpmu.FwpmLayerDestroyEnumHandle0
title: FwpmLayerDestroyEnumHandle0 function
author: windows-sdk-content
description: Frees a handle returned by FwpmFilterCreateEnumHandle0.
old-location: fwp\fwpmlayerdestroyenumhandle0_func.htm
old-project: fwp
ms.assetid: 351112c2-7ede-4aa7-8ef3-673efeb1c7bb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FwpmLayerDestroyEnumHandle0, FwpmLayerDestroyEnumHandle0 function [Filtering], fwp.fwpmlayerdestroyenumhandle0_func, fwpmu/FwpmLayerDestroyEnumHandle0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmLayerDestroyEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmLayerDestroyEnumHandle0 function


## -description


The <b>FwpmLayerDestroyEnumHandle0</b> function frees a handle returned by <a href="https://msdn.microsoft.com/fd8ffa91-a205-441c-9145-da8b441cef28">FwpmFilterCreateEnumHandle0</a>.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle of a layer enumeration created by a call to <a href="https://msdn.microsoft.com/94738168-9f02-420a-96cd-b7c3f6418c6f">FwpmLayerCreateEnumHandle0</a>.


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



<b>FwpmLayerDestroyEnumHandle0</b> is a specific implementation of FwpmLayerDestroyEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/94738168-9f02-420a-96cd-b7c3f6418c6f">FwpmLayerCreateEnumHandle0</a>
 

 

