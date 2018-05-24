---
UID: NF:netfw.INetFwRules.Add
title: INetFwRules::Add
author: windows-driver-content
description: The Add method adds a new rule to the collection.
old-location: ics\inetfwrules_add.htm
old-project: ICS
ms.assetid: c81bdf56-df71-425a-93d2-1fbae5ab536e
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: Add, Add method [ICS/ICF], Add method [ICS/ICF],INetFwRules interface, INetFwRules interface [ICS/ICF],Add method, INetFwRules.Add, INetFwRules::Add, ics.inetfwrules_add, netfw/INetFwRules::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: netfw.h
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
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FirewallAPI.dll
api_name:
-	INetFwRules.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwRules::Add


## -description


The <b>Add</b> method adds a new rule to the collection.


## -parameters




### -param rule [in]

Rule to be added to the collection via an <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> object.


## -returns



<h3>C++</h3>

						If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed because a parameter was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The  method failed because the  object is already in the collection.

</td>
</tr>
</table>
 

<h3>VB</h3>

						If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed because a parameter was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The  method failed because the  object is already in the collection.

</td>
</tr>
</table>
 




## -remarks



If a rule with the same rule identifier as the one being submitted already exists, the existing rule is overwritten.

Adding a firewall rule with a <a href="https://msdn.microsoft.com/8c1bccc6-3c8d-401c-8e9f-e88a4a60e3f4">LocalAppPackageId</a> specified can lead to unexpected behavior and is not supported.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>



<a href="https://msdn.microsoft.com/4908a5f2-4093-4f2d-8e68-fe4b2e552b13">INetFwRules</a>
 

 

