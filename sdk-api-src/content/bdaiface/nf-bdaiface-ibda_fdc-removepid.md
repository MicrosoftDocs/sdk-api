---
UID: NF:bdaiface.IBDA_FDC.RemovePid
title: IBDA_FDC::RemovePid
author: windows-sdk-content
description: Removes one or more packet identifiers (PIDs) from the MPEG flow.
old-location: mstv\ibda_fdc_removepid.htm
tech.root: mstv
ms.assetid: 1277726c-6443-416c-a5d4-044d5f885af7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_FDC interface [Microsoft TV Technologies],RemovePid method, IBDA_FDC.RemovePid, IBDA_FDC::RemovePid, RemovePid, RemovePid method [Microsoft TV Technologies], RemovePid method [Microsoft TV Technologies],IBDA_FDC interface, bdaiface/IBDA_FDC::RemovePid, mstv.ibda_fdc_removepid
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
 - IBDA_FDC.RemovePid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_FDC::RemovePid


## -description


Removes one or more packet identifiers (PIDs) from the MPEG flow.


## -parameters




### -param PidsToRemove [in]

A comma-separated list of PIDs to remove.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 This command causes the device to send a delete_flow_req Application Protocol Data Unit (APDU).




## -see-also




<a href="https://msdn.microsoft.com/8b7a07fd-99e9-4f8e-9211-109689f2f892">IBDA_FDC</a>
 

 

