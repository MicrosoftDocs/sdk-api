---
UID: NF:shobjidl_core.IShellLibrary.SetOptions
title: IShellLibrary::SetOptions (shobjidl_core.h)
description: Sets the library options.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","SetOptions method","IShellLibrary.SetOptions","IShellLibrary::SetOptions","SetOptions","SetOptions method [Windows Shell]","SetOptions method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_SetOptions","shell.IShellLibrary_SetOptions","shobjidl_core/IShellLibrary::SetOptions"]
old-location: shell\IShellLibrary_SetOptions.htm
tech.root: shell
ms.assetid: 8bec0c71-3170-4ff9-aa87-4880d6ac7e32
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],SetOptions method, IShellLibrary.SetOptions, IShellLibrary::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SetOptions, shell.IShellLibrary_SetOptions, shobjidl_core/IShellLibrary::SetOptions
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IShellLibrary::SetOptions
 - shobjidl_core/IShellLibrary::SetOptions
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
 - IShellLibrary.SetOptions
---

# IShellLibrary::SetOptions


## -description

Sets the library options.

## -parameters

### -param lofMask [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a></b>

A bitmask  that specifies   the   <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a> values  to change in  this call.

### -param lofOptions [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a></b>

A bitmask that specifies the new value of each  <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a>  value to change. <b>LIBRARYOPTIONFLAGS</b>  values that are not set in <i>lofMask</i> are not changed by this call.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a> is a bitwise enumerator, which means that more than one option flag can be set.

To change an option value, you must set the option value that you want to change in <i>lofMask</i> and then set or clear the value of the option in <i>lofOptions</i>.


#### Examples

The following example clears the LOF_PINNEDTONAVPANE library option.


```cpp

LIBRARYOPTIONFLAGS	maskValue;
LIBRARYOPTIONFLAGS optionValue;
HRESULT	hr = E_FAIL;

// set the maskValue variable to indicate
// which option value to change
maskValue = LOF_PINNEDTONAVPANE;

// set the optionValue variable to indicate
// the new value of the option
optionValue = ~LOF_PINNEDTONAVPANE;

// call the method
hr = library->SetOptions (maskValue, optionValue);
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>