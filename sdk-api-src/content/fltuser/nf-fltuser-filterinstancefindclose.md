---
UID: NF:fltuser.FilterInstanceFindClose
title: FilterInstanceFindClose function (fltuser.h)
description: The FilterInstanceFindClose function closes the specified minifilter instance search handle. The FilterInstanceFindFirst and FilterInstanceFindNext functions use this search handle to locate instances of a minifilter.
helpviewer_keywords: ["FilterInstanceFindClose","FilterInstanceFindClose function [Installable File System Drivers]","FltWin32ApiRef_e9ea0ce5-7e02-40df-8e12-5b7fb8b0a189.xml","fltuser/FilterInstanceFindClose","ifsk.filterinstancefindclose"]
old-location: ifsk\filterinstancefindclose.htm
tech.root: ifsk
ms.assetid: f4b066ca-4154-425d-85f6-682dc7460117
ms.date: 12/05/2018
ms.keywords: FilterInstanceFindClose, FilterInstanceFindClose function [Installable File System Drivers], FltWin32ApiRef_e9ea0ce5-7e02-40df-8e12-5b7fb8b0a189.xml, fltuser/FilterInstanceFindClose, ifsk.filterinstancefindclose
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
 - FilterInstanceFindClose
 - fltuser/FilterInstanceFindClose
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
 - FilterInstanceFindClose
---

# FilterInstanceFindClose function


## -description

The <b>FilterInstanceFindClose</b> function closes the specified minifilter instance search handle. The <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindnext">FilterInstanceFindNext</a> functions use this search handle to locate instances of a minifilter.

## -parameters

### -param hFilterInstanceFind [in]

Minifilter instance search handle to close. This handle must have been opened by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>.

## -returns

<b>FilterInstanceFindClose</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

After the <b>FilterInstanceFindClose</b> function is called, the minifilter instance search handle specified by the <i>hFilterInstanceFind</i> parameter cannot be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a> or <b>FilterInstanceFindClose</b>. 

Use <b>FilterInstanceFindClose</b> to close handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>. Use <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstanceclose">FilterInstanceClose</a> to close handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancecreate">FilterInstanceCreate</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstanceclose">FilterInstanceClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancecreate">FilterInstanceCreate</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindnext">FilterInstanceFindNext</a>