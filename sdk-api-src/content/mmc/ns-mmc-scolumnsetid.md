---
UID: NS:mmc._SColumnSetID
title: SColumnSetID (mmc.h)
description: The SColumnSetID structure is introduced in MMC 1.2.
helpviewer_keywords: ["SColumnSetID","SColumnSetID structure [MMC]","_slate_scolumnsetid","mmc.scolumnsetid","mmc/SColumnSetID"]
old-location: mmc\scolumnsetid.htm
tech.root: mmc
ms.assetid: eb08f699-74bc-445d-96b7-678abbd366b3
ms.date: 12/05/2018
ms.keywords: SColumnSetID, SColumnSetID structure [MMC], _slate_scolumnsetid, mmc.scolumnsetid, mmc/SColumnSetID
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: SColumnSetID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SColumnSetID
 - mmc/_SColumnSetID
 - SColumnSetID
 - mmc/SColumnSetID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SColumnSetID
---

# SColumnSetID structure


## -description

The 
<b>SColumnSetID</b> structure is introduced in MMC 1.2.

The 
<b>SColumnSetID</b> structure is used by the 
<a href="/previous-versions/windows/desktop/mmc/ccf-column-set-id">CCF_COLUMN_SET_ID</a> clipboard format.

The 
<b>SColumnSetID</b> structure contains an array of bytes that represent the node ID.

## -struct-fields

### -field dwFlags

Reserved for future use. Must be 0.

### -field cBytes

The count of bytes in the <b>id</b> array.

### -field id

The bytes that contains the column set ID.

## -remarks

For details on using the 
<b>SColumnSetID</b> structure with the CCF_COLUMN_SET_ID clipboard format, see 
<a href="/previous-versions/windows/desktop/mmc/ccf-column-set-id">CCF_COLUMN_SET_ID</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-column-set-id">CCF_COLUMN_SET_ID</a>