---
UID: NF:fltuser.FilterVolumeInstanceFindClose
title: FilterVolumeInstanceFindClose function (fltuser.h)
description: The FilterVolumeInstanceFindClose function closes the specified volume instance search handle. FilterVolumeInstanceFindFirst and FilterVolumeInstanceFindNext use this search handle to locate instances on a volume.
helpviewer_keywords: ["FilterVolumeInstanceFindClose","FilterVolumeInstanceFindClose function [Installable File System Drivers]","FltWin32ApiRef_5cdcef76-2a6d-4d64-9af6-09b050073573.xml","fltuser/FilterVolumeInstanceFindClose","ifsk.filtervolumeinstancefindclose"]
old-location: ifsk\filtervolumeinstancefindclose.htm
tech.root: ifsk
ms.assetid: 4c56bcea-c027-4607-8531-da971e43e763
ms.date: 12/05/2018
ms.keywords: FilterVolumeInstanceFindClose, FilterVolumeInstanceFindClose function [Installable File System Drivers], FltWin32ApiRef_5cdcef76-2a6d-4d64-9af6-09b050073573.xml, fltuser/FilterVolumeInstanceFindClose, ifsk.filtervolumeinstancefindclose
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterVolumeInstanceFindClose
 - fltuser/FilterVolumeInstanceFindClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterVolumeInstanceFindClose
---

# FilterVolumeInstanceFindClose function


## -description

The <b>FilterVolumeInstanceFindClose</b> function closes the specified volume instance search handle. <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindfirst">FilterVolumeInstanceFindFirst</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindnext">FilterVolumeInstanceFindNext</a> use this search handle to locate instances on a volume.

## -parameters

### -param hVolumeInstanceFind [in]

Volume instance search handle to close. This handle must have been opened by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindfirst">FilterVolumeInstanceFindFirst</a>.

## -returns

<b>FilterVolumeInstanceFindClose</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

After the <b>FilterVolumeInstanceFindClose</b> function is called, the handle specified by the <i>hVolumeInstanceFind</i> parameter cannot be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindnext">FilterVolumeInstanceFindNext</a> or <b>FilterVolumeInstanceFindClose</b>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindfirst">FilterVolumeInstanceFindFirst</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindnext">FilterVolumeInstanceFindNext</a>