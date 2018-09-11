---
UID: NF:bdaiface.IBDA_FDC.GetTableSection
title: IBDA_FDC::GetTableSection
author: windows-sdk-content
description: Gets the latest table section.
old-location: mstv\ibda_fdc_gettablesection.htm
tech.root: mstv
ms.assetid: 77c83234-c752-4f94-a3f1-cc62a5da894a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTableSection, GetTableSection method [Microsoft TV Technologies], GetTableSection method [Microsoft TV Technologies],IBDA_FDC interface, IBDA_FDC interface [Microsoft TV Technologies],GetTableSection method, IBDA_FDC.GetTableSection, IBDA_FDC::GetTableSection, bdaiface/IBDA_FDC::GetTableSection, mstv.ibda_fdc_gettablesection
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
 - IBDA_FDC.GetTableSection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_FDC::GetTableSection


## -description


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693347(v=VS.85).aspx">IBDA_FDC</a>
 

 

