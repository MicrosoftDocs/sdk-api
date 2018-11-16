---
UID: NF:bdaiface.IBDA_FDC.AddTid
title: IBDA_FDC::AddTid
author: windows-sdk-content
description: Adds one or more table identifiers (TIDs) to the MPEG flow.
old-location: mstv\ibda_fdc_addtid.htm
tech.root: mstv
ms.assetid: 2cd39bbc-106b-4411-bc42-a1adc360e121
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddTid, AddTid method [Microsoft TV Technologies], AddTid method [Microsoft TV Technologies],IBDA_FDC interface, IBDA_FDC interface [Microsoft TV Technologies],AddTid method, IBDA_FDC.AddTid, IBDA_FDC::AddTid, bdaiface/IBDA_FDC::AddTid, mstv.ibda_fdc_addtid
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
 - IBDA_FDC.AddTid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_FDC.AddTid
: 
---

# IBDA_FDC::AddTid


## -description


Adds one or more table identifiers (TIDs) to the MPEG flow.


## -parameters




### -param TidsToAdd [in]

A comma-separated list of TIDs.


### -param CurrentTidList [out]

Receives a comma-separated list of the current TIDs. The caller must release the string by calling <b>SysFreeString</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693347(v=VS.85).aspx">IBDA_FDC</a>
 

 

