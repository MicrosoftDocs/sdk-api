---
UID: NF:bindlink.CreateBindLink
tech.root: fs
title: CreateBindLink (bindlink.h)
ms.date: 05/01/2023
targetos: Windows
description: This API allows admins to create a bind link between a virtual path and a backing path.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: bindlink.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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

The following example illustrates how a user can configure a link from C:\\test to C:\\Windows.

```cpp
#include <iostream>
#include <wil\resource.h>
#include <string>
#include <iostream>
#include <filesystem>
#include <bindlink.h>   

using namespace std::filesystem;

void print_file_status(const path& p, file_status s)
{
    std::cout << p;
    switch (s.type())
    {
    case file_type::regular:
        std::cout << " is a regular file\n";
        break;
    
    case file_type::directory:
        std::cout << " is a directory\n";
        break;
    
    case file_type::block:
        std::cout << " is a block device\n";
        break;
    
    case file_type::character:
        std::cout << " is a character device\n";
        break;
    
    case file_type::fifo:
        std::cout << " is a named IPC pipe\n";
        break;
   
    case file_type::socket:
        std::cout << " is a named IPC socket\n";
        break;
    
    case file_type::symlink:
        std::cout << " is a symlink\n";
        break;
    
    case file_type::junction:
        std::cout << " is a junction\n";
        break;
    
    case file_type::unknown:
        std::cout << " type could not be determined\n";
        break;
    
    case file_type::not_found:
        std::cout << " could not be found.\n";
        break;
    
    default:
        std::cerr << " failed to determine file type.\n";
        break;
    }
}

void listDirectoryElements(const std::wstring& dirPath)
{
    path directoryPath(dirPath);

    for (const auto& entry : directory_iterator(directoryPath))
    {
        print_file_status(entry.path(), entry.status());  
    }
}    

int wmain(int argc, wchar_t* argv[])
{
    constexpr PCWSTR virtPath = L"C:\\test";
    constexpr PCWSTR backingPath = L"C:\\Windows";
    auto bindLinkFlags = CREATE_BIND_LINK_FLAG_NONE;
    HRESULT hr = S_OK;
        
    hr = CreateBindLink(virtPath, targetPath, bindLinkFlags, 0, nullptr);

    if(FAILED(hr))
    {
        std::cerr << "CreateBindLink Failed with Err: " << hr;
        return hr;
    }
  
    std::cout << "Link Configured!\n";

    // Now that the link is created, virtPath can be traversed as any other path on the system.
    // Since virtPath maps to C:\Windows, listing contents of virtPath resembles contents of 
    // C:\Windows. 

    try 
    {
        listDirectoryElements(std::wstring(virtPath));
    }
    catch (const std::filesystem::filesystem_error& ex) 
    {
        std::cerr
            << "what():  " << ex.what() << '\n'
            << "path1(): " << ex.path1() << '\n'
            << "path2(): " << ex.path2() << '\n'
            << "code().value():    " << ex.code().value() << '\n'
            << "code().message():  " << ex.code().message() << '\n'
            << "code().category(): " << ex.code().category().name() << '\n';
    }
    catch (const std::system_error& ex) 
    {
        std::cerr
            << "Caught system_error with code " << ex.code()
            << "what():  " << ex.what() << '\n';
    }
    catch (const std::exception& ex) 
    {
        std::cerr
            << "what():  " << ex.what() << '\n';
    }
}
```

## -see-also

[RemoveBindLink](nf-bindlink-removebindlink.md)
