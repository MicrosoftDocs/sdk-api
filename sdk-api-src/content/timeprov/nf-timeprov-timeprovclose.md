---
UID: NF:timeprov.TimeProvClose
title: TimeProvClose function (timeprov.h)
description: A callback function that is called by the time provider manager to shut down the time provider.
helpviewer_keywords: ["TimeProvClose","TimeProvClose callback","TimeProvClose callback function","_win32_timeprovclose","base.timeprovclose","timeprov/TimeProvClose"]
old-location: base\timeprovclose.htm
tech.root: winprog
ms.assetid: ca8f5c8b-8c46-46eb-8d15-4c0c8a8437dd
ms.date: 12/05/2018
ms.keywords: TimeProvClose, TimeProvClose callback, TimeProvClose callback function, _win32_timeprovclose, base.timeprovclose, timeprov/TimeProvClose
req.header: timeprov.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TimeProvClose
 - timeprov/TimeProvClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Timeprov.h
api_name:
 - TimeProvClose
---

# TimeProvClose function


## -description

A  callback function that is called by the time provider manager to shut down the time provider.

## -parameters

### -param hTimeProv [in]

A handle to the time provider. The 
<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a> function receives this handle.

## -returns

If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.

## -remarks

The provider should clean up its resources and terminate its operation. When the function returns, the time provider manager can unload the DLL. Therefore, the handle to the time provider is no longer valid and should not be used again.


#### Examples

For an example, see <a href="/windows/desktop/SysInfo/sample-time-provider">Sample Time Provider</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a>