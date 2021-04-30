---
UID: NF:fltuser.FilterVolumeFindClose
title: FilterVolumeFindClose function (fltuser.h)
description: The FilterVolumeFindClose function closes the specified volume search handle. FilterVolumeFindFirst and FilterVolumeFindNext use this search handle to locate volumes.
helpviewer_keywords: ["FilterVolumeFindClose","FilterVolumeFindClose function [Installable File System Drivers]","FltWin32ApiRef_bdc13aec-06f6-4e73-abcb-ca452040e600.xml","fltuser/FilterVolumeFindClose","ifsk.filtervolumefindclose"]
old-location: ifsk\filtervolumefindclose.htm
tech.root: ifsk
ms.assetid: 18b707a0-2d34-46a9-a77c-b356aba44d72
ms.date: 12/05/2018
ms.keywords: FilterVolumeFindClose, FilterVolumeFindClose function [Installable File System Drivers], FltWin32ApiRef_bdc13aec-06f6-4e73-abcb-ca452040e600.xml, fltuser/FilterVolumeFindClose, ifsk.filtervolumefindclose
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
 - FilterVolumeFindClose
 - fltuser/FilterVolumeFindClose
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
 - FilterVolumeFindClose
---

# FilterVolumeFindClose function


## -description

The <b>FilterVolumeFindClose</b> function closes the specified volume search handle. <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindfirst">FilterVolumeFindFirst</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindnext">FilterVolumeFindNext</a> use this search handle to locate volumes.

## -parameters

### -param hVolumeFind [in]

Volume search handle to close. This handle must have been previously opened by <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindfirst">FilterVolumeFindFirst</a>.

## -returns

<b>FilterVolumeFindClose</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

After the <b>FilterVolumeFindClose</b> function is called, the handle specified by the <i>hVolumeFind</i> parameter cannot be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindnext">FilterVolumeFindNext</a> or <b>FilterVolumeFindClose</b>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindfirst">FilterVolumeFindFirst</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindnext">FilterVolumeFindNext</a>