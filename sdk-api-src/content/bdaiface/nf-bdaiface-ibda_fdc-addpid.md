---
UID: NF:bdaiface.IBDA_FDC.AddPid
title: IBDA_FDC::AddPid
author: windows-driver-content
description: Adds one or more packet identifiers (PIDs) to the MPEG flow.
old-location: mstv\ibda_fdc_addpid.htm
old-project: mstv
ms.assetid: 28bc019c-1b5e-43e2-9fb4-7274d9c0e275
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: AddPid, AddPid method [Microsoft TV Technologies], AddPid method [Microsoft TV Technologies],IBDA_FDC interface, IBDA_FDC interface [Microsoft TV Technologies],AddPid method, IBDA_FDC.AddPid, IBDA_FDC::AddPid, bdaiface/IBDA_FDC::AddPid, mstv.ibda_fdc_addpid
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_FDC.AddPid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_FDC::AddPid


## -description


Adds one or more packet identifiers (PIDs) to the MPEG flow.


## -parameters




### -param PidsToAdd [in]

A comma-separated list of PIDs.


### -param RemainingFilterEntries [out]

Receives the number of remaining MPEG flows on the device.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 This command causes the device to send a new_flow_req Application Protocol Data Unit (APDU).




## -see-also




<a href="https://msdn.microsoft.com/8b7a07fd-99e9-4f8e-9211-109689f2f892">IBDA_FDC</a>
 

 

