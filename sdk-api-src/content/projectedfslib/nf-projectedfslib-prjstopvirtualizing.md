---
UID: NF:projectedfslib.PrjStopVirtualizing
title: PrjStopVirtualizing function
author: windows-sdk-content
description: Stops a running ProjFS virtualization instance, making it unavailable to service I/O or involve callbacks on the provider.
old-location: projfs\prjstopvirtualizing.htm
tech.root: ProjFS
ms.assetid: D01BF7C5-1EAC-446A-BCE5-A6EF46A5443D
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PrjStopVirtualizing, PrjStopVirtualizing function, ProjFS.prjstopvirtualizing, projectedfslib/PrjStopVirtualizing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PrjStopVirtualizing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PrjStopVirtualizing
: 
---

# PrjStopVirtualizing function


## -description


Stops a running ProjFS virtualization instance, making it unavailable to service I/O or involve callbacks on the provider.


## -parameters




### -param namespaceVirtualizationContext [in]

An opaque handle for the virtualization instance.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



