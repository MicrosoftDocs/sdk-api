---
UID: NF:bdaiface.IBDA_MUX.GetPidList
title: IBDA_MUX::GetPidList
author: windows-sdk-content
description: Gets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.
old-location: mstv\ibda_mux_getpidlist.htm
old-project: mstv
ms.assetid: 92b13d40-4841-45ce-b232-5e29a93d71c5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetPidList, GetPidList method [Microsoft TV Technologies], GetPidList method [Microsoft TV Technologies],IBDA_MUX interface, IBDA_MUX interface [Microsoft TV Technologies],GetPidList method, IBDA_MUX.GetPidList, IBDA_MUX::GetPidList, bdaiface/IBDA_MUX::GetPidList, mstv.ibda_mux_getpidlist
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_MUX.GetPidList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_MUX::GetPidList


## -description


Gets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.


## -parameters




### -param pulPidListCount [in, out]

On input, specifies the size, in array elements, of the <i>pbPidListBuffer</i> array. On output, receives the number of PIDs.


### -param pbPidListBuffer [in, out]

Pointer to an array of <a href="https://msdn.microsoft.com/50355317-7133-445c-9990-ab536801e555">BDA_MUX_PIDLISTITEM</a> structures. The method fills in the array with the list of PIDs.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_NOT_SUFFICIENT_BUFFER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>pbPidListBuffer</i> array is too small.

</td>
</tr>
</table>
 




## -remarks



If the <i>pbPidListBuffer</i> array is too small, the method returns <b>E_NOT_SUFFICIENT_BUFFER</b> and sets the required size in the <i>pulPidListCount</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/5dde7b14-d5a4-4db5-b91f-d6bfd4be269d">IBDA_MUX</a>
 

 

