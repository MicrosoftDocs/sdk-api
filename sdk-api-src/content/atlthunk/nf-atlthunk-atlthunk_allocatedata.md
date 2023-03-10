---
UID: NF:atlthunk.AtlThunk_AllocateData
title: AtlThunk_AllocateData function (atlthunk.h)
description: Allocates space in memory for an ATL thunk.
helpviewer_keywords: ["AtlThunk_AllocateData","AtlThunk_AllocateData function","atlthunk/AtlThunk_AllocateData","base.atlthunk_allocatedata"]
old-location: base\atlthunk_allocatedata.htm
tech.root: base
ms.assetid: D306E6CB-72D4-4820-885E-175FC8500954
ms.date: 12/05/2018
ms.keywords: AtlThunk_AllocateData, AtlThunk_AllocateData function, atlthunk/AtlThunk_AllocateData, base.atlthunk_allocatedata
req.header: atlthunk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Atlthunk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AtlThunk_AllocateData
 - atlthunk/AtlThunk_AllocateData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - atlthunk.dll
api_name:
 - AtlThunk_AllocateData
---

# AtlThunk_AllocateData function


## -description

Allocates space in memory for an ATL thunk.



## -returns

If the function succeeds, the return value is an ATL thunk.

If the function fails, the return value is NULL. To get extended error information, call GetLastError.

