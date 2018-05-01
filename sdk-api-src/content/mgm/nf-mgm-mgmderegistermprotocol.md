---
UID: NF:mgm.MgmDeRegisterMProtocol
title: MgmDeRegisterMProtocol function
author: windows-driver-content
description: The MgmDeRegisterMProtocol function deregisters a client handle obtained from a call to MgmRegisterMProtocol.
old-location: rras\mgmderegistermprotocol.htm
old-project: RRAS
ms.assetid: e9b2613e-4e52-4993-81dd-0be50a072db6
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: MgmDeRegisterMProtocol, MgmDeRegisterMProtocol function [RAS], _mpr_mgmderegistermprotocol, mgm/MgmDeRegisterMProtocol, rras.mgmderegistermprotocol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MGM_ENUM_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	MgmDeRegisterMProtocol
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: GDI+ 1.1
---

# MgmDeRegisterMProtocol function


## -description


The 
<b>MgmDeRegisterMProtocol</b> function deregisters a client handle obtained from a call to 
<a href="https://msdn.microsoft.com/a9b5f5f3-6e54-4a97-b3e7-e9e026947116">MgmRegisterMProtocol</a>.


## -parameters




### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="https://msdn.microsoft.com/a9b5f5f3-6e54-4a97-b3e7-e9e026947116">MgmRegisterMProtocol</a>.


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
<a href="https://msdn.microsoft.com/501970f7-7728-4a83-8f4b-207579d65d01">MgmReleaseInterfaceOwnership</a>.




## -see-also




<a href="https://msdn.microsoft.com/a9b5f5f3-6e54-4a97-b3e7-e9e026947116">MgmRegisterMProtocol</a>



<a href="https://msdn.microsoft.com/501970f7-7728-4a83-8f4b-207579d65d01">MgmReleaseInterfaceOwnership</a>
 

 

