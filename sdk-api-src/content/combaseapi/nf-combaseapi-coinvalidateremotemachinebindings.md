---
UID: NF:combaseapi.CoInvalidateRemoteMachineBindings
title: CoInvalidateRemoteMachineBindings function (combaseapi.h)
description: Tells the service control manager to flush any cached RPC binding handles for the specified computer.
helpviewer_keywords: ["CoInvalidateRemoteMachineBindings","CoInvalidateRemoteMachineBindings function [COM]","_com_CoInvalidateRemoteMachineBindings","com.coinvalidateremotemachinebindings","combaseapi/CoInvalidateRemoteMachineBindings"]
old-location: com\coinvalidateremotemachinebindings.htm
tech.root: com
ms.assetid: 6d0fa512-a9e9-44ff-929d-00b9c826da99
ms.date: 12/05/2018
ms.keywords: CoInvalidateRemoteMachineBindings, CoInvalidateRemoteMachineBindings function [COM], _com_CoInvalidateRemoteMachineBindings, com.coinvalidateremotemachinebindings, combaseapi/CoInvalidateRemoteMachineBindings
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoInvalidateRemoteMachineBindings
 - combaseapi/CoInvalidateRemoteMachineBindings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoInvalidateRemoteMachineBindings
---

# CoInvalidateRemoteMachineBindings function


## -description

Tells the <a href="/windows/desktop/Services/service-control-manager">service control manager</a> to flush any cached RPC binding handles for the specified computer.

Only administrators may call this function.

## -parameters

### -param pszMachineName [in]

The computer name for which binding handles should be flushed, or an empty string to signify that all handles in the cache should be flushed.

## -returns

This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_S_MACHINENAMENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the specified computer name was not found or that the binding handle cache was empty, indicating that an empty string was passed instead of a specific computer name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the caller was not an administrator for this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a <b>NULL</b> value was passed for <i>pszMachineName</i>.


</td>
</tr>
</table>

## -remarks

The OLE Service Control Manager is used by COM to send component activation requests to other machines. To do this, the OLE Service Control Manager maintains a cache of RPC binding handles to send activation requests to computer, keyed by computer name. Under normal circumstances, this works well, but in some scenarios, such as Web farms and load-balancing situations, the ability to purge this cache of specific handles might be needed in order to facilitate rebinding to a different physical server by the same name. <b>CoInvalidateRemoteMachineBindings</b> is used for this purpose.

The OLE Service Control Manager will flush unused binding handles over time. It is not necessary to call <b>CoInvalidateRemoteMachineBindings</b> to do this.