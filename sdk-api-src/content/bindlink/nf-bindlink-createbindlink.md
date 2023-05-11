---
UID: NF:bindlink.CreateBindLink
tech.root: fs
title: CreateBindLink (bindlink.h)
ms.date: 05/01/2023
targetos: Windows
description: This API allows admins to create a bind link between a virtual path and a backing path.
prerelease: true
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
 - CreateBindLink
f1_keywords:
 - CreateBindLink
 - bindlink/CreateBindLink
dev_langs:
 - c++
helpviewer_keywords:
 - CreateBindLink
---

## -description

This API allows admins to create a bind link between a virtual path and a backing path. The virtual path is always local while the backing path could be local or remote (a network share, for example). The parent of the *virtualPath* should be visible for the link creation to succeed. Both the virtual path and the backing path can represent files or directories. The *backingPath* for a prior link can be a *virtualPath* for a subsequent link as well. **CreateBindLink** can only be called by a user with Administrator privileges. Once created, a bind link exists system-wide, and it lasts until it is deleted by calling [RemoveBindLink](nf-bindlink-removebindlink.md), or until the system is shut down.

## -parameters

### -param virtualPath

The virtual path to be used to create the bind link.

### -param backingPath

The backing path to be used to create the bind link.

### -param createBindLinkFlags

These flags can change the default bind link behavior to suit the needs of the user. See [CREATE_BIND_LINK_FLAGS](ne-bindlink-create_bind_link_flags.md) for more details.

### -param exceptionCount

The number of exceptions provided in the *exceptionPaths* parameter.

### -param exceptionPaths

The exception paths to be excluded from the bind link. Note that exceptions do not apply to anchorless links since anchorless virtual paths have no descendants by definition and, therefore, have no paths that qualify. The API will return an error if there is an attempt to pass exceptions to anchorless link.

## -returns

## -remarks

Bind links are transparent to the applications and whilst these links exist, all operations apply to the backing path. As a result, **DeleteFile** or **RemoveDirectory** will act upon the backing path, effectively deleting the backing path but not the link. This API will fail if the user does not have Administrator privileges, if the user does not have permissions to open the virtual path or the backing path, if the backing path doesn’t exist, if another link exists for the virtual path, or if there is an internal failure while setting up the link. Specifically, the admin user should be able to attach the filter (permissions for **FilterAttach**), connect to the filter port (permissions for **FilterConnectCommunicationPort**) and access the root of the backing path or else the api will fail with **ERROR_ACCESS_DENIED**.

If an app tries to follow the link to a backing path that was deleted after the link was setup, the app will see *ERROR_FILE_NOT_FOUND**. Later if the backing path is created again, the link will now apply to this new backing path. If a file were to be created at the *virtualPath* while the link exists, it would show up at the *virtualPath* if the link exists but is physically created at the backing path. When the link is removed, the file would only appear at the backing path and would no longer show up at the *virtualPath*. This applies to all the kinds of links described below.

Depending on whether the virtual path is present on-disk, the resulting link will either be an anchorless link or a shadow link.

#### Anchorless Links

Anchorless links are bind links that are created when the virtual path does not exist on the disk before the link is created. When this sort of link is created, the virtual path is synthesized in-memory and appears like a regular path in the filesystem. Note that to create such a bind link, the parent of the virtual path must exist either as an on-disk directory or as a previously created link. For example, to use C:\\Foo\\Bar as a virtual path, C:\\Foo must be an on-disk directory or previously created as the virtual path for another link. Since there is no parent for a volume, there cannot be an anchorless link to a volume that doesn’t exist. For example, creating a bind link with a virtual path "Z:" would fail if there wasn't already a volume named "Z".

#### Shadow Links

A shadow link is one where the virtual path exists on the volume prior to the link being created. When such a virtual path is used to create a link, the contents of the virtual path are hidden while the contents of the backing path become visible at the virtual path. For example:

- C:\\Foo exists on disk with two files Cat.txt and Dog.txt
- C:\\Bar exists on disk with two files Cow.txt and Mouse.txt

When a link is created with C:\\Foo as the virtual path and C:\\Bar as the backing path, the C:\\Foo path will then show Cow.txt and Mouse.txt to all users while Cat.txt and Dog.txt will be hidden, until the link is removed.

## -examples

The following sample shows how to create and remove bind links.

```cpp
#include <wil\resource.h>
#include <string>
#include <iostream>
#include <iomanip>
#if !__has_include(<bindlink.h>)
#error This sample requires the Windows SDK version 10.0.25314.0 or higher.
#endif
#include <bindlink.h>

void usage(FILE* fp)
{
    fprintf(fp, "Usage: BindLink command command-parameters [command-options]\n");
    fprintf(fp, "Commands:\n");
    fprintf(fp, "   CREATE virtPath targetPath\n");
    fprintf(fp, "   REMOVE virtPath\n");
    fprintf(fp, "Command options for CREATE:\n");
    fprintf(fp, "   /merge             merge bind links\n");
    fprintf(fp, "   /read-only         read only bind links\n");
}

void printErrorDetails(PCWSTR command, HRESULT hr)
{
    std::wcout << command << " failed with HRESULT 0x" << std::hex << std::setw(8) << std::setfill(L'0') << hr << "\n";
    wchar_t buffer[32768];
    if (FormatMessageW(FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, nullptr, hr,
        0, buffer, ARRAYSIZE(buffer), nullptr))
    {
        std::wcout << buffer << "\n";
    }
}

int handleCreateCommand(int argc, wchar_t* argv[])
{
    // argv[0] = program name
    // argv[1] = "CREATE"
    // argv[2] = virtPath
    // argv[3] = backingPath
    // argv[4...] = options

    if (argc < 4)
    {
        usage(stderr);
        return 1;
    }

    PCWSTR virtPath = argv[2];
    PCWSTR backingPath = argv[3];

    auto bindLinkFlags = CREATE_BIND_LINK_FLAG_NONE;

    for (int index = 4; index < argc && argv[index][0] == L'/'; ++index)
    {
        if (!_wcsicmp(argv[index], L"/read-only"))
        {
            WI_SetFlag(bindLinkFlags, CREATE_BIND_LINK_FLAG_READ_ONLY);
        }
        else if (!_wcsicmp(argv[index], L"/merge"))
        {
            WI_SetFlag(bindLinkFlags, CREATE_BIND_LINK_FLAG_MERGED);
        }
        else
        {
            usage(stderr);
            return 1;
        }
    }

    auto hr = CreateBindLink(virtPath, backingPath, bindLinkFlags, 0, nullptr);

    if (FAILED(hr))
    {
        printErrorDetails(L"CreateBindLink", hr);
        return hr;
    }

    std::wcout << "Bind Link Created.\n";
    std::wcout << "\"" << virtPath << "\" draws content from \"" << backingPath << "\"\n";

    return 0;
}

int handleRemoveCommand(int argc, wchar_t* argv[])
{
    // argv[0] = program name
    // argv[1] = "REMOVE"
    // argv[2] = virtPath

    if (argc != 3)
    {
        usage(stderr);
        return 1;
    }

    PCWSTR virtPath = argv[2];

    auto hr = RemoveBindLink(virtPath);

    if (FAILED(hr))
    {
        printErrorDetails(L"RemoveBindLink", hr);
        return hr;
    }

    std::wcout << "Bind Link for \"" << virtPath << "\" removed.\n";

    return 0;
}

int wmain(int argc, wchar_t* argv[])
{
    if (argc < 2) {
        usage(stderr);
        return 1;
    }

    if (!_wcsicmp(argv[1], L"CREATE"))
    {
        return handleCreateCommand(argc, argv);
    }
    else if (!_wcsicmp(argv[1], L"REMOVE"))
    {
        return handleRemoveCommand(argc, argv);
    }
    else
    {
        usage(stderr);
        return 1;
    }

    return 0;
}
```

## -see-also

[RemoveBindLink](nf-bindlink-removebindlink.md)
