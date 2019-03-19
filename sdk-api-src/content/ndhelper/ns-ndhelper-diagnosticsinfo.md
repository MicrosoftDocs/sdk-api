---
UID: NS:ndhelper.tagDiagnosticsInfo
title: DiagnosticsInfo (ndhelper.h)
author: windows-sdk-content
description: The DiagnosticsInfo structure contains the estimate of diagnosis time, and flags for invocation.
old-location: ndf\diagnosticsinfo.htm
tech.root: NDF
ms.assetid: c84cc4ef-ff47-447e-b216-b704cb02719a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDiagnosticsInfo, DiagnosticsInfo, DiagnosticsInfo structure [NDF], DiagnosticsInfo,*PDiagnosticsInfo, DiagnosticsInfo,*PDiagnosticsInfo structure [NDF], ndf.diagnosticsinfo, ndhelper/DiagnosticsInfo"
ms.topic: struct
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ndhelper.h
api_name:
 - DiagnosticsInfo, *PDiagnosticsInfo
product: Windows
targetos: Windows
req.typenames: DiagnosticsInfo, *PDiagnosticsInfo
req.redist: 
---

# DiagnosticsInfo structure


## -description


The <b>DiagnosticsInfo</b> structure contains the estimate of diagnosis time, and flags for invocation.


## -struct-fields




### -field cost

Type: <b>long</b>

The length of time, in seconds, that the diagnosis should take to complete. A value of zero or a negative value  means the cost is negligible. Any positive value will cause the engine to adjust the overall diagnostics process.


### -field flags

Type: <b>ULONG</b>

Reserved.

