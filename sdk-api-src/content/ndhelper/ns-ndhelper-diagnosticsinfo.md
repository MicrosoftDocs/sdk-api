---
UID: NS:ndhelper.tagDiagnosticsInfo
title: DiagnosticsInfo (ndhelper.h)
description: The DiagnosticsInfo structure contains the estimate of diagnosis time, and flags for invocation.
helpviewer_keywords: ["*PDiagnosticsInfo","DiagnosticsInfo","DiagnosticsInfo structure [NDF]","DiagnosticsInfo","*PDiagnosticsInfo","DiagnosticsInfo","*PDiagnosticsInfo structure [NDF]","ndf.diagnosticsinfo","ndhelper/DiagnosticsInfo"]
old-location: ndf\diagnosticsinfo.htm
tech.root: NDF
ms.assetid: c84cc4ef-ff47-447e-b216-b704cb02719a
ms.date: 12/05/2018
ms.keywords: '*PDiagnosticsInfo, DiagnosticsInfo, DiagnosticsInfo structure [NDF], DiagnosticsInfo,*PDiagnosticsInfo, DiagnosticsInfo,*PDiagnosticsInfo structure [NDF], ndf.diagnosticsinfo, ndhelper/DiagnosticsInfo'
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
targetos: Windows
req.typenames: DiagnosticsInfo, *PDiagnosticsInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDiagnosticsInfo
 - ndhelper/tagDiagnosticsInfo
 - PDiagnosticsInfo
 - ndhelper/PDiagnosticsInfo
 - DiagnosticsInfo
 - ndhelper/DiagnosticsInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndhelper.h
api_name:
 - DiagnosticsInfo, *PDiagnosticsInfo
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

