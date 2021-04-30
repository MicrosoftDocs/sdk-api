---
UID: NF:fltuser.FilterInstanceClose
title: FilterInstanceClose function (fltuser.h)
description: The FilterInstanceClose function closes a minifilter instance handle opened by FilterInstanceCreate.
helpviewer_keywords: ["FilterInstanceClose","FilterInstanceClose function [Installable File System Drivers]","FltWin32ApiRef_aed3c694-a4bb-4804-9171-4d89cabd666d.xml","fltuser/FilterInstanceClose","ifsk.filterinstanceclose"]
old-location: ifsk\filterinstanceclose.htm
tech.root: ifsk
ms.assetid: a0605b02-a5eb-4e7f-9659-0f0f538ea153
ms.date: 12/05/2018
ms.keywords: FilterInstanceClose, FilterInstanceClose function [Installable File System Drivers], FltWin32ApiRef_aed3c694-a4bb-4804-9171-4d89cabd666d.xml, fltuser/FilterInstanceClose, ifsk.filterinstanceclose
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
 - FilterInstanceClose
 - fltuser/FilterInstanceClose
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
 - FilterInstanceClose
---

# FilterInstanceClose function


## -description

The <b>FilterInstanceClose</b> function closes a minifilter instance handle opened by <b>FilterInstanceCreate</b>.

## -parameters

### -param hInstance [in]

Minifilter instance handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancecreate">FilterInstanceCreate</a>.

## -returns

<b>FilterInstanceClose</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

After the <b>FilterInstanceClose</b> function is called, the minifilter instance handle specified by the <i>hFilterInstanceFind</i> parameter is no longer valid and cannot safely be used. 

Use <b>FilterInstanceClose</b> to close handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancecreate">FilterInstanceCreate</a>. Use <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindclose">FilterInstanceFindClose</a> to close handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancecreate">FilterInstanceCreate</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindclose">FilterInstanceFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>