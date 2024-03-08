---
UID: NF:bdaiface.IBDA_FDC.GetTableSection
title: IBDA_FDC::GetTableSection (bdaiface.h)
description: Gets the latest table section.
helpviewer_keywords: ["GetTableSection","GetTableSection method [Microsoft TV Technologies]","GetTableSection method [Microsoft TV Technologies]","IBDA_FDC interface","IBDA_FDC interface [Microsoft TV Technologies]","GetTableSection method","IBDA_FDC.GetTableSection","IBDA_FDC::GetTableSection","bdaiface/IBDA_FDC::GetTableSection","mstv.ibda_fdc_gettablesection"]
old-location: mstv\ibda_fdc_gettablesection.htm
tech.root: mstv
ms.assetid: 77c83234-c752-4f94-a3f1-cc62a5da894a
ms.date: 12/05/2018
ms.keywords: GetTableSection, GetTableSection method [Microsoft TV Technologies], GetTableSection method [Microsoft TV Technologies],IBDA_FDC interface, IBDA_FDC interface [Microsoft TV Technologies],GetTableSection method, IBDA_FDC.GetTableSection, IBDA_FDC::GetTableSection, bdaiface/IBDA_FDC::GetTableSection, mstv.ibda_fdc_gettablesection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_FDC::GetTableSection
 - bdaiface/IBDA_FDC::GetTableSection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_FDC.GetTableSection
---

# IBDA_FDC::GetTableSection


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the latest table section.

## -parameters

### -param Pid [out]

Receives the packet identifier (PID) of the table.

### -param MaxBufferSize [in]

The size of the <i>SecBuffer</i> array, in bytes.

### -param ActualSize [out]

Receives the number of bytes that the method copies into the  <i>SecBuffer</i> array.

### -param SecBuffer [out]

A byte array, allocated by the caller, that receives the table section.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_fdc">IBDA_FDC</a>