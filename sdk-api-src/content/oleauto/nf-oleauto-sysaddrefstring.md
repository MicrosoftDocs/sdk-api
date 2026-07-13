---
UID: NF:oleauto.SysAddRefString
title: SysAddRefString function (oleauto.h)
description: Increases the pinning reference count for the specified string by one.
helpviewer_keywords: ["SysAddRefString","SysAddRefString function [Automation]","automat.sysaddrefstring","oleauto/SysAddRefString"]
old-location: automat\sysaddrefstring.htm
tech.root: automat
ms.assetid: 9AE274F1-1517-4D55-B9AE-D75169404880
ms.date: 12/05/2018
ms.keywords: SysAddRefString, SysAddRefString function [Automation], automat.sysaddrefstring, oleauto/SysAddRefString
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
 - SysAddRefString
 - oleauto/SysAddRefString
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
 - SysAddRefString
---

# SysAddRefString function


## -description

<div class="alert"><b>Note</b>  You should only call <b>SysAddRefString</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Increases the  pinning reference count for the specified string by one.

## -parameters

### -param bstrString [in]

The string for which the pinning reference count should increase. While that count remains greater than 0, the memory for the string is prevented from being freed by calls to the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Strings with the <b>BSTR</b> data type have not traditionally had a reference count. All existing usage of these strings will continue to work with no changes. The <b>SysAddRefString</b> and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysreleasestring">SysReleaseString</a> functions add the ability to use reference counting to pin the string into memory before calling from an untrusted script into an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> method that may not expect the script to free that memory before the method returns, so that the script cannot force the code for that method into accessing memory that has been freed. After such a method safely returns, the pinning references should be released by calling <b>SysReleaseString</b>.

## -see-also

<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysreleasestring">SysReleaseString</a>