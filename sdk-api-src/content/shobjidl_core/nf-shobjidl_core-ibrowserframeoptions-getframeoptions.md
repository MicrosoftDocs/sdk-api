---
UID: NF:shobjidl_core.IBrowserFrameOptions.GetFrameOptions
title: IBrowserFrameOptions::GetFrameOptions (shobjidl_core.h)
description: Retrieves the available browser frame view options.
helpviewer_keywords: ["GetFrameOptions","GetFrameOptions method [Windows Shell]","GetFrameOptions method [Windows Shell]","IBrowserFrameOptions interface","IBrowserFrameOptions interface [Windows Shell]","GetFrameOptions method","IBrowserFrameOptions.GetFrameOptions","IBrowserFrameOptions::GetFrameOptions","_shell_IBrowserFrameOptions_GetFrameOptions","shell.IBrowserFrameOptions_GetFrameOptions","shobjidl_core/IBrowserFrameOptions::GetFrameOptions"]
old-location: shell\IBrowserFrameOptions_GetFrameOptions.htm
tech.root: shell
ms.assetid: 4f0e9f69-92e5-4fec-bdfa-b37d594ff5fe
ms.date: 12/05/2018
ms.keywords: GetFrameOptions, GetFrameOptions method [Windows Shell], GetFrameOptions method [Windows Shell],IBrowserFrameOptions interface, IBrowserFrameOptions interface [Windows Shell],GetFrameOptions method, IBrowserFrameOptions.GetFrameOptions, IBrowserFrameOptions::GetFrameOptions, _shell_IBrowserFrameOptions_GetFrameOptions, shell.IBrowserFrameOptions_GetFrameOptions, shobjidl_core/IBrowserFrameOptions::GetFrameOptions
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBrowserFrameOptions::GetFrameOptions
 - shobjidl_core/IBrowserFrameOptions::GetFrameOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IBrowserFrameOptions.GetFrameOptions
---

# IBrowserFrameOptions::GetFrameOptions


## -description

Retrieves the available browser frame view options.

## -parameters

### -param dwMask [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_browserframeoptions">BROWSERFRAMEOPTIONS</a></b>

Specifies the options requested as a bitwise combination of one or more of the constants of enumeration type <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_browserframeoptions">BROWSERFRAMEOPTIONS</a>.

### -param pdwOptions [out]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_browserframeoptions">BROWSERFRAMEOPTIONS</a>*</b>

When this method returns, contains the options that the view  can enable (for example, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> ). This value is not optional and is always equal to, or a subset of, the options specified by <i>dwMask</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the method succeeds, the return value is S_OK and <i>pdwOptions</i> contains the subset of available view options.  If the method fails, <i>pdwOptions</i> is set to BFO_NONE.