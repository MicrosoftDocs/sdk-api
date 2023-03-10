---
UID: NF:oleauto.SysReleaseString
title: SysReleaseString function (oleauto.h)
description: Decreases the pinning reference count for the specified string by one. When that count reaches 0, the memory for that string is no longer prevented from being freed.
helpviewer_keywords: ["SysReleaseString","SysReleaseString function [Automation]","automat.sysreleasestring","oleauto/SysReleaseString"]
old-location: automat\sysreleasestring.htm
tech.root: automat
ms.assetid: D4905794-A4EA-4925-A4B2-92C8BF6EDFD0
ms.date: 12/05/2018
ms.keywords: SysReleaseString, SysReleaseString function [Automation], automat.sysreleasestring, oleauto/SysReleaseString
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mincore.lib
req.dll: Oleaut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SysReleaseString
 - oleauto/SysReleaseString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleaut32.dll
api_name:
 - SysReleaseString
---

# SysReleaseString function


## -description

<div class="alert"><b>Note</b>  You should only call <b>SysReleaseString</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Decreases the pinning reference count for the specified string by one. When that count reaches 0, the memory for that string is no longer prevented from being freed.

## -parameters

### -param bstrString [in]

The string for which the  pinning reference count should decrease.

## -remarks

A call to the <b>SysReleaseString</b> function should match every previous call to the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysaddrefstring">SysAddRefString</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysaddrefstring">SysAddRefString</a>