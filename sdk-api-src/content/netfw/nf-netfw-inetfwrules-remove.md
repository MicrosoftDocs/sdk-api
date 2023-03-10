---
UID: NF:netfw.INetFwRules.Remove
title: INetFwRules::Remove (netfw.h)
description: The Remove method removes a rule from the collection.
helpviewer_keywords: ["INetFwRules interface [ICS/ICF]","Remove method","INetFwRules.Remove","INetFwRules::Remove","Remove","Remove method [ICS/ICF]","Remove method [ICS/ICF]","INetFwRules interface","ics.inetfwrules_remove","netfw/INetFwRules::Remove"]
old-location: ics\inetfwrules_remove.htm
tech.root: ics
ms.assetid: 70bd45c7-b5ab-43b3-afd4-2abb2a80ff0f
ms.date: 12/05/2018
ms.keywords: INetFwRules interface [ICS/ICF],Remove method, INetFwRules.Remove, INetFwRules::Remove, Remove, Remove method [ICS/ICF], Remove method [ICS/ICF],INetFwRules interface, ics.inetfwrules_remove, netfw/INetFwRules::Remove
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
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwRules::Remove
 - netfw/INetFwRules::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRules.Remove
---

# INetFwRules::Remove


## -description

The <b>Remove</b> method removes a rule from the collection.

## -parameters

### -param name [in]

Name of the rule  to remove from the collection.

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
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

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
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
</table>

## -remarks

If a rule specified by the <i>name</i> parameter does not exist in the collection, the <b>Remove</b> method has no effect.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules">INetFwRules</a>