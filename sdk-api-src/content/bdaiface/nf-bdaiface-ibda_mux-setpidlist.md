---
UID: NF:bdaiface.IBDA_MUX.SetPidList
title: IBDA_MUX::SetPidList
author: windows-sdk-content
description: Sets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.
old-location: mstv\ibda_mux_setpidlist.htm
tech.root: mstv
ms.assetid: 2d77086c-2321-434d-bf24-b4eac395825b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_MUX interface [Microsoft TV Technologies],SetPidList method, IBDA_MUX.SetPidList, IBDA_MUX::SetPidList, SetPidList, SetPidList method [Microsoft TV Technologies], SetPidList method [Microsoft TV Technologies],IBDA_MUX interface, bdaiface/IBDA_MUX::SetPidList, mstv.ibda_mux_setpidlist
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_MUX.SetPidList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_MUX::SetPidList


## -description


Sets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.


## -parameters




### -param ulPidListCount [in]

The number of elements in the <i>pbPidListBuffer</i> array.


### -param pbPidListBuffer [in]

Pointer to an array of <a href="https://msdn.microsoft.com/50355317-7133-445c-9990-ab536801e555">BDA_MUX_PIDLISTITEM</a> structures.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5dde7b14-d5a4-4db5-b91f-d6bfd4be269d">IBDA_MUX</a>
 

 

