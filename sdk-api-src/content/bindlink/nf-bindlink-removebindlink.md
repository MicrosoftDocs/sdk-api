---
UID: NF:bindlink.RemoveBindLink
tech.root: fs
title: RemoveBindLink (bindlink.h)
ms.date: 04/24/2023
targetos: Windows
description: This API allows a user to remove a link that was previously created by calling CreateBindLink.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: bindlink.dll
req.header: bindlink.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: bindlink.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - bindlink.h
api_name:
 - RemoveBindLink
f1_keywords:
 - RemoveBindLink
 - bindlink/RemoveBindLink
dev_langs:
 - c++
helpviewer_keywords:
 - RemoveBindLink
---

## -description

This API allows a user to remove a link that was previously created by calling [CreateBindLink](nf-bindlink-createbindlink.md).

## -parameters

### -param virtualPath

The virtual path for which the bind link is to be removed.

## -returns

## -remarks

This API will fail if the user does not have Administrator privileges, or if the user does not have permission to access the virtual path, or if the link being deleted is the ancestor of an existing link. The API will also fail if the link doesn’t exist or due to another internal error. If an app is in the middle of traversing the virtual path while **RemoveBindLink** is called, the resulting behavior will depend on where each of the threads are in the process (i.e., this is a race between the link being deleted and the file/directory being accessed).

Note that nested links must be removed in deepest-first order. This means the deepest virtual path must be removed before ancestor virtual paths can be    removed. Unrelated services that create the links and remove the links are expected to be respectful of each other's personal space and limit their mappings to paths under their control.

## Examples

The following example shows how a user can remove a previously created link on `C:\\test`.

```cpp
#include <iostream>
#include <wil\resource.h>
#include <bindlink.h>

int wmain(int argc, wchar_t* argv[])
{
    constexpr PCWSTR virtPath = L"C:\test";
    HRESULT hr = S_OK;

    hr = RemoveBindLink(virtPath);

    if(FAILED(hr))
    {
        std::cerr << "RemoveBindLink Failed with Err: " << hr;
        return hr;
    }

    std::cout << "Link Deleted!\n";
}
```

For a full example of how to use the **CreateBindLink** and **RemoveBindLink** APIs, see the [bind link example](/windows/win32/bindlink/bindlink-example) page.

## -see-also

[CreateBindLink](nf-bindlink-createbindlink.md)
