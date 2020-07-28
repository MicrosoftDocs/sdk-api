---
UID: NF:projectedfslib.PrjStopVirtualizing
title: PrjStopVirtualizing function (projectedfslib.h)
description: Stops a running ProjFS virtualization instance, making it unavailable to service I/O or involve callbacks on the provider.
helpviewer_keywords: ["PrjStopVirtualizing","PrjStopVirtualizing function","ProjFS.prjstopvirtualizing","projectedfslib/PrjStopVirtualizing"]
old-location: projfs\prjstopvirtualizing.htm
tech.root: ProjFS
ms.assetid: D01BF7C5-1EAC-446A-BCE5-A6EF46A5443D
ms.date: 12/05/2018
ms.keywords: PrjStopVirtualizing, PrjStopVirtualizing function, ProjFS.prjstopvirtualizing, projectedfslib/PrjStopVirtualizing
f1_keywords:
- projectedfslib/PrjStopVirtualizing
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# PrjStopVirtualizing function


## -description


Stops a running ProjFS virtualization instance, making it unavailable to service I/O or involve callbacks on the provider.


## -parameters




### -param namespaceVirtualizationContext [in]

An opaque handle for the virtualization instance.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



