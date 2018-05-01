---
UID: NF:rrascfg.IEAPProviderConfig.Initialize
title: IEAPProviderConfig::Initialize method
author: windows-driver-content
description: The system calls the Initialize method to initialize an EAP configuration session with the specified computer.
old-location: eap\ieapproviderconfig_initialize.htm
old-project: EAP
ms.assetid: 6d347387-7f8f-478b-a115-f6960e6f856e
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: IEAPProviderConfig, IEAPProviderConfig interface [EAP], Initialize method, IEAPProviderConfig::Initialize, Initialize method [EAP], Initialize method [EAP], IEAPProviderConfig interface, Initialize,IEAPProviderConfig.Initialize, _eap_ieapproviderconfig_initialize, eap.ieapproviderconfig_initialize, rrascfg/IEAPProviderConfig::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rrascfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProxyFileInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Rrascfg.h
api_name:
-	IEAPProviderConfig.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEAPProviderConfig::Initialize method


## -description


The system calls the <b>Initialize</b> method to initialize an EAP configuration session with the specified computer.


## -parameters




### -param pszMachineName

Pointer to a null-terminated string that contains the name of the computer on which to configure EAP. String length is not limited.


### -param dwEapTypeId

Specifies the EAP for which to initialize a configuration session.


### -param puConnectionParam

Pointer to an unsigned integer variable. On successful return, the value of this variable identifies this configuration session.


## -returns



If the function succeeds, the return value should be <b>S_OK</b>.

If the function fails, the return value should be one of the following codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Non-specific error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method failed because it was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



The configuration UI should allow the user to configure the EAP provider on a remote computer. Establish the connection to the remote computer during the call to <b>Initialize</b>.

The DLL that implements 
<a href="https://msdn.microsoft.com/1e0283b7-ceb3-4c8a-99d9-1a1f1eb5eeb0">IEAPProviderConfig</a> can support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies the  authentication protocol to initialize a configuration session for.




## -see-also




<a href="https://msdn.microsoft.com/1f720c0c-d490-48af-830f-9a25cbc24014">EAP Interfaces</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/1e0283b7-ceb3-4c8a-99d9-1a1f1eb5eeb0">IEAPProviderConfig</a>



<a href="https://msdn.microsoft.com/ba07f5c6-0b76-489f-b787-2965710cd1c5">IEAPProviderConfig::RouterInvokeConfigUI</a>



<a href="https://msdn.microsoft.com/23b64f95-1f21-4e81-a094-081a95057aef">IEAPProviderConfig::RouterInvokeCredentialsUI</a>



<a href="https://msdn.microsoft.com/95d98664-e108-41d5-8ed0-49867563df43">IEAPProviderConfig::ServerInvokeConfigUI</a>



<a href="https://msdn.microsoft.com/f96ffa3f-cd3c-4979-87b3-1a2afb7a3621">IEAPProviderConfig::Uninitialize</a>
 

 

