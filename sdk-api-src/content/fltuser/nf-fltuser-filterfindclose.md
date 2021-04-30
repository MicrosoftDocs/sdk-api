---
UID: NF:fltuser.FilterFindClose
title: FilterFindClose function (fltuser.h)
description: The FilterFindClose function closes the specified minifilter search handle. The FilterFindFirst and FilterFindNext functions use this search handle to locate minifilters.
helpviewer_keywords: ["FilterFindClose","FilterFindClose function [Installable File System Drivers]","FltWin32ApiRef_37b77edb-bee8-40ca-803f-4091417ef714.xml","fltuser/FilterFindClose","ifsk.filterfindclose"]
old-location: ifsk\filterfindclose.htm
tech.root: ifsk
ms.assetid: 053c06b0-3bfd-436c-ab98-14c55e66da53
ms.date: 12/05/2018
ms.keywords: FilterFindClose, FilterFindClose function [Installable File System Drivers], FltWin32ApiRef_37b77edb-bee8-40ca-803f-4091417ef714.xml, fltuser/FilterFindClose, ifsk.filterfindclose
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
 - FilterFindClose
 - fltuser/FilterFindClose
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
 - FilterFindClose
---

# FilterFindClose function


## -description

The <b>FilterFindClose</b> function closes the specified minifilter search handle. The <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a> functions use this search handle to locate minifilters.

## -parameters

### -param hFilterFind [in]

Minifilter search handle to close. This handle must have been opened by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>.

## -returns

<b>FilterFindClose</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

After the <b>FilterFindClose</b> function is called, the minifilter search handle specified by the <i>hFilterFind</i> parameter cannot be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a> or <b>FilterFindClose</b>. 

Use <b>FilterFindClose</b> to close handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>. Use <a href="/windows/desktop/api/fltuser/nf-fltuser-filterclose">FilterClose</a> to close handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtercreate">FilterCreate</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterclose">FilterClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtercreate">FilterCreate</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a>