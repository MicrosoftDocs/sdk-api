---
UID: NF:mgm.MgmDeRegisterMProtocol
title: MgmDeRegisterMProtocol function (mgm.h)
description: The MgmDeRegisterMProtocol function deregisters a client handle obtained from a call to MgmRegisterMProtocol.
helpviewer_keywords: ["MgmDeRegisterMProtocol","MgmDeRegisterMProtocol function [RAS]","_mpr_mgmderegistermprotocol","mgm/MgmDeRegisterMProtocol","rras.mgmderegistermprotocol"]
old-location: rras\mgmderegistermprotocol.htm
tech.root: RRAS
ms.assetid: e9b2613e-4e52-4993-81dd-0be50a072db6
ms.date: 12/05/2018
ms.keywords: MgmDeRegisterMProtocol, MgmDeRegisterMProtocol function [RAS], _mpr_mgmderegistermprotocol, mgm/MgmDeRegisterMProtocol, rras.mgmderegistermprotocol
req.header: mgm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MgmDeRegisterMProtocol
 - mgm/MgmDeRegisterMProtocol
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - MgmDeRegisterMProtocol
---

# MgmDeRegisterMProtocol function


## -description

The 
<b>MgmDeRegisterMProtocol</b> function deregisters a client handle obtained from a call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmregistermprotocol">MgmRegisterMProtocol</a>.

## -parameters

### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmregistermprotocol">MgmRegisterMProtocol</a>.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function. The client did not first release the interfaces it owns.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle to a client.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

A multicast routing protocol must not call this function until it has released ownership of all the interfaces the protocol owns by calling 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmreleaseinterfaceownership">MgmReleaseInterfaceOwnership</a>.

## -see-also

<a href="/windows/desktop/api/mgm/nf-mgm-mgmregistermprotocol">MgmRegisterMProtocol</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmreleaseinterfaceownership">MgmReleaseInterfaceOwnership</a>