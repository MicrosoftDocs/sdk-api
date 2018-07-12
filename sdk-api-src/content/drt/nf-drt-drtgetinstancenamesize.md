---
UID: NF:drt.DrtGetInstanceNameSize
title: DrtGetInstanceNameSize function
author: windows-sdk-content
description: The DrtGetInstanceNameSize function returns the size of the Distributed Routing Table instance name.
old-location: p2p\drtgetinstancenamesize.htm
old-project: p2psdk
ms.assetid: b600ee27-bcea-4496-888f-1300f74d41e4
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DrtGetInstanceNameSize, DrtGetInstanceNameSize function [Peer Networking], drt/DrtGetInstanceNameSize, p2p.drtgetinstancenamesize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
tech.root: 
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtGetInstanceNameSize
product: Windows
targetos: Windows
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
---

# DrtGetInstanceNameSize function


## -description


The <b>DrtGetInstanceNameSize</b> function returns the size of the Distributed Routing Table instance name.


## -parameters




### -param hDrt [in]

Handle to the target DRT instance.


### -param pulcbInstanceNameSize [out]

The length of the DRT instance name.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pulcbInstanceNameSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hDrt</i> handle is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>
 

 

