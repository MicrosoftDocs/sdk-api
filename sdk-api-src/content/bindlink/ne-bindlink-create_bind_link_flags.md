---
UID: NE:bindlink.CREATE_BIND_LINK_FLAGS
tech.root: fs
title: CREATE_BIND_LINK_FLAGS (bindlink.h)
ms.date: 04/24/2023
targetos: Windows
description: These flags can be passed in to CreateBindLink to change the default bind link behavior to suit the needs of the user.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: bindlink.h
req.dll: bindlink.dll
req.lib: bindlink.lib
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - bindlink.h
api_name:
 - CREATE_BIND_LINK_FLAGS
f1_keywords:
 - CREATE_BIND_LINK_FLAGS
 - bindlink/CREATE_BIND_LINK_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - CREATE_BIND_LINK_FLAGS
---

## -description

These flags can be passed in to [CreateBindLink](nf-bindlink-createbindlink.md) to change the default bind link behavior to suit the needs of the user.

## -enum-fields

### -field CREATE_BIND_LINK_FLAG_NONE

`0x00000000`

No bind link flags are specified.

### -field CREATE_BIND_LINK_FLAG_READ_ONLY

`0x00000001`

Read Only links are bind links where the users on the system are prevented from making changes to files that reside in the backing path if they are accessed through the virtual path. This means that a user with permission to modify a file on the backing path can still modify that file if they access it through the backing path, but not if they access it through the virtual path. Normally, the permissions of the backing path apply as such when the corresponding virtual path is accessed, however when **READ_ONLY** flag is used the "write" permissions are masked off. This ensures that applications see that the file is **READ_ONLY**.

Note that the read only restriction only applies to files that reside at the backing path on disk. If the link is merged and files that are originally from the virtual directory path are visible, they will remain modifiable. For example:

C:\\Foo exists on disk with a file Cat.txt
C:\\Bar exists on disk with a file Cow.txt

When a link is created with C:\\Foo as the virtual path and C:\\Bar as the backing path and the link is marked read-only and merged, both Cat.txt and Cow.txt will be visible at C:\\Foo, however, Cat.txt will be modifiable while Cow.txt will not be modifiable.

### -field CREATE_BIND_LINK_FLAG_MERGED

`0x00000002`

A merged link is like a shadow link, except the existing content in the virtual path is merged with backing path.

Let’s consider the prior example for shadow link once again, with the addition of this flag. For example:

- C:\\Foo exists on disk with two files Cat.txt and Dog.txt
- C:\\Bar exists on disk with two files Cow.txt and Mouse.txt

When a link is created with C:\\Foo as the virtual path and C:\\Bar as the backing path with the flag **CREATE_BIND_LINK_FLAG_MERGED**, C:\Foo path will show Cat.txt, Dog.txt, Cow.txt and Mouse.txt.

Note that merged links only apply when the virtual path is a directory. In the case where a file appears in both the backing path and the virtual path, the file in the backing path takes precedence (i.e., the file in the virtual path is masked). This applies recursively for all directories within the virtual path. Since the merge applies to directories, if the *virtualPath* and the *backingPath* both have a directory with the same name at the same level, the directory will be merged as an outcome of the link. If the link wasn’t a merged link the directory in the backing path will take precedence and override the directory in the *virtualPath*. If a file were created at the merged path when the merged link exists, it will be physically created at the backing path (as is the case with any bind link) and will override a file with the same name at the *virtualPath*.

Let’s consider the following directory structures:

- c:\Foo\Sub\Foo_sub.txt
- c:\Bar\Sub\Bar_sub.txt

And two different links:

- {c:\\Foo is linked to c:\\Bar WITHOUT merge}. In this case c:\\Foo\\Sub will only show Bar_sub.txt.
- {c:\\Foo is linked to c:\\Bar WITH merge}. In this case c:\\Foo\\Sub will show both Foo_sub.txt and Bar_sub.txt.

Since bind links are path-based links, if a file is replaced, modified, or deleted/recreated in the backing path after the link is created, the virtual path will point to the file that exists at the time the link is being followed. It happens because the link is resolved at the time a file is opened. Accordingly, if a file from the backing path was masking a file in the virtual path due to the link and if the file in the backing path was deleted, a subsequent open will open the file in the virtual path.

## -remarks

## -see-also

[CreateBindLink](nf-bindlink-createbindlink.md)
