---
UID: NF:ual.UalStop
title: UalStop function (ual.h)
description: Stops a User Access Logging (UAL) session.
helpviewer_keywords: ["UalStop","UalStop function [User Access Logging]","ual.ualstop","ual/UalStop"]
old-location: ual\ualstop.htm
tech.root: ual
ms.assetid: 142A0C96-2D53-4C31-9847-D6D5313C841E
ms.date: 12/05/2018
ms.keywords: UalStop, UalStop function [User Access Logging], ual.ualstop, ual/UalStop
req.header: ual.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ualapi.lib
req.dll: Ualapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UalStop
 - ual/UalStop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ualapi.dll
api_name:
 - UalStop
---

# UalStop function


## -description

Stops a User Access Logging (UAL) session.

## -parameters

### -param Data [in]

A pointer to an <a href="/windows/desktop/api/ual/ns-ual-ual_data_blob">UAL_DATA_BLOB</a> structure that specifies session information.

Only the <b>RoleGuid</b> property of the <a href="/windows/desktop/api/ual/ns-ual-ual_data_blob">UAL_DATA_BLOB</a> structure is required. All other members can be null.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/ual/nf-ual-ualinstrument">UalInstrument</a>



<a href="/previous-versions/windows/desktop/api/ual/nf-ual-ualstart">UalStart</a>