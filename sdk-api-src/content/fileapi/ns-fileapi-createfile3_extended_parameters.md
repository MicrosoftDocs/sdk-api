---
UID: NS:fileapi._CREATEFILE3_EXTENDED_PARAMETERS
tech.root: fs
title: CREATEFILE3_EXTENDED_PARAMETERS structure (fileapi.h)
ms.date: 04/10/2025
targetos: Windows
description: 
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: fileapi.h
req.include-header: Windows.h
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 24H2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2025 [desktop apps \| UWP apps]
req.target-type: 
req.typenames: CREATEFILE3_EXTENDED_PARAMETERS, *PCREATEFILE3_EXTENDED_PARAMETERS, *LPCREATEFILE3_EXTENDED_PARAMETERS
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - _CREATEFILE3_EXTENDED_PARAMETERS
 - PCREATEFILE3_EXTENDED_PARAMETERS
 - CREATEFILE3_EXTENDED_PARAMETERS
f1_keywords:
 - _CREATEFILE3_EXTENDED_PARAMETERS
 - fileapi/_CREATEFILE3_EXTENDED_PARAMETERS
 - PCREATEFILE3_EXTENDED_PARAMETERS
 - fileapi/PCREATEFILE3_EXTENDED_PARAMETERS
 - CREATEFILE3_EXTENDED_PARAMETERS
 - fileapi/CREATEFILE3_EXTENDED_PARAMETERS
dev_langs:
 - c++
helpviewer_keywords:
 - _CREATEFILE3_EXTENDED_PARAMETERS
---

## -description

Contains optional extended parameters for [CreateFile3](nf-fileapi-createfile3.md).

## -struct-fields

### -field dwSize

Contains the size of this structure, `sizeof(CREATEFILE3_EXTENDED_PARAMETERS)`.

### -field dwFileAttributes

The file or device attributes and flags, **FILE_ATTRIBUTE_NORMAL** being the most common default value for files.

This parameter can include any combination of the available file attributes (**FILE_ATTRIBUTE_\***). All other file attributes override **FILE_ATTRIBUTE_NORMAL**.

> [!NOTE]
> When [CreateFile3](nf-fileapi-createfile3.md) opens an existing file, it generally combines the file flags with the file attributes of the existing file, and ignores any file attributes supplied as part of *dwFlagsAndAttributes*. Special cases are detailed in [Creating and Opening Files](/windows/win32/fileio/creating-and-opening-files).

Some of the following file attributes and flags may only apply to files and not necessarily all other types of devices that [CreateFile3](nf-fileapi-createfile3.md) can open. For additional information, see the **Remarks** section of the **CreateFile3** reference page and [Creating and Opening Files](/windows/win32/fileio/creating-and-opening-files).

For more advanced access to file attributes, see [SetFileAttributes](nf-fileapi-setfileattributesa.md). For a complete list of all file attributes with their values and descriptions, see [File Attribute Constants](/windows/win32/fileio/file-attribute-constants).

| Attribute | Meaning |
|-----------|---------|
| **FILE_ATTRIBUTE_ARCHIVE**<br/>`32 (0x20)` | The file should be archived. Applications use this attribute to mark files for backup or removal. |
| **FILE_ATTRIBUTE_ENCRYPTED**<br/>`16384 (0x4000)` | The file or directory is encrypted. For a file, this means that all data in the file is encrypted. For a directory, this means that encryption is the default for newly created files and subdirectories. For more information, see <a href="/windows/win32/FileIO/file-encryption">File Encryption</a>.<br/><br/>This flag has no effect if **FILE_ATTRIBUTE_SYSTEM** is also specified.<br/><br/>This flag is not supported on Home, Home Premium, Starter, or ARM editions of Windows.<br/><br/>This flag is not supported when called from a Windows Store app. |
| **FILE_ATTRIBUTE_HIDDEN**<br/>`2 (0x2)` | The file is hidden. Do not include it in an ordinary directory listing. |
| **FILE_ATTRIBUTE_INTEGRITY_STREAM**<br/>`32768 (0x8000)` | A file or directory that is configured with integrity. For a file, all data streams in the file have integrity. For a directory, integrity is the default for newly created files and subdirectories, unless the caller specifies otherwise.<br/><br/>This flag is only supported on the ReFS file system. |
| **FILE_ATTRIBUTE_NORMAL**<br/>`128 (0x80)` | The file does not have other attributes set. This attribute is valid only if used alone. |
| **FILE_ATTRIBUTE_OFFLINE**<br/>`4096 (0x1000)` | The data of a file is not immediately available. This attribute indicates that file data is physically moved to offline storage. This attribute is used by Remote Storage, the hierarchical storage management software. Applications should not arbitrarily change this attribute. |
| **FILE_ATTRIBUTE_READONLY**<br/>`1 (0x1)` | The file is read only. Applications can read the file, but cannot write to or delete it. |
| **FILE_ATTRIBUTE_SYSTEM**<br/>`4 (0x4)` | The file is part of or used exclusively by an operating system. |
| **FILE_ATTRIBUTE_TEMPORARY**<br/>`256 (0x100)` | The file is being used for temporary storage.<br/><br/>For more information, see the **Caching Behavior** section of this topic. |

### -field dwFileFlags

This parameter can contain combinations of flags (**FILE_FLAG_\***) for control of file or device caching behavior, access modes, and other special-purpose flags.

| Flag | Meaning |
|------|---------|
| **FILE_FLAG_DISALLOW_PATH_REDIRECTS**<br/>`0x00010000` | Prevent paths from being redirected by reparse points or symbolic links. |
| **FILE_FLAG_BACKUP_SEMANTICS**<br/>`0x02000000` | The file is being opened or created for a backup or restore operation. The system ensures that the calling process overrides file security checks when the process has **SE_BACKUP_NAME** and **SE_RESTORE_NAME** privileges. For more information, see [Changing Privileges in a Token](/windows/win32/SecBP/changing-privileges-in-a-token).<br/><br/>You must set this flag to obtain a handle to a directory. A directory handle can be passed to some functions instead of a file handle. For more information, see the [Remarks](#-remarks) section. |
| **FILE_FLAG_DELETE_ON_CLOSE**<br/>`0x04000000` | The file is to be deleted immediately after all of its handles are closed, which includes the specified handle and any other open or duplicated handles.<br/><br/>If there are existing open handles to a file, the call fails unless they were all opened with the **FILE_SHARE_DELETE** share mode.<br/><br/>Subsequent open requests for the file fail, unless the **FILE_SHARE_DELETE** share mode is specified. |
| **FILE_FLAG_IGNORE_IMPERSONATED_DEVICEMAP**<br/>`0x00020000` | A device map is a mapping between DOS device names and devices in the system, and is used when resolving DOS names. Separate device maps exists for each user in the system, and users can manage their own device maps. Typically during impersonation, the impersonated user's device map would be used. However, when this flag is set, the process user's device map is used instead. |
| **FILE_FLAG_NO_BUFFERING**<br/>`0x20000000` | The file or device is being opened with no system caching for data reads and writes. This flag does not affect hard disk caching or memory mapped files.<br/><br/>There are strict requirements for successfully working with files opened with [CreateFile3](nf-fileapi-createfile3.md) using the **FILE_FLAG_NO_BUFFERING** flag, for details see [File Buffering](/windows/win32/fileio/file-buffering). |
| **FILE_FLAG_OPEN_NO_RECALL**<br/>`0x00100000` | The file data is requested, but it should continue to be located in remote storage. It should not be transported back to local storage. This flag is for use by remote storage systems. |
| **FILE_FLAG_OPEN_REPARSE_POINT**<br/>`0x00200000` | Normal [reparse point](/windows/win32/fileio/reparse-points) processing will not occur; [CreateFile3](nf-fileapi-createfile3.md) will attempt to open the reparse point. When a file is opened, a file handle is returned, whether or not the filter that controls the reparse point is operational.<br/><br/>This flag cannot be used with the **CREATE_ALWAYS** flag.<br/><br/>If the file is not a reparse point, then this flag is ignored.<br/><br/>For more information, see the [Remarks](#-remarks) section. |
| **FILE_FLAG_OPEN_REQUIRING_OPLOCK**<br/>`0x00040000` | The file is being opened and an opportunistic lock (oplock) on the file is being requested as a single atomic operation. The file system checks for oplocks before it performs the create operation, and will fail the create with a last error code of **ERROR_CANNOT_BREAK_OPLOCK** if the result would be to break an existing oplock.<br/><br/>If you use this flag and your call to the [CreateFile3](nf-fileapi-createfile3.md) function successfully returns, the first operation you should perform on the file handle is to request an oplock by calling the [DeviceIOControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function and then pass in [FSCTL_REQUEST_OPLOCK](../winioctl/ni-winioctl-fsctl_request_oplock.md) or one of the other [Opportunistic Lock Operations](/windows/win32/fileio/opportunistic-lock-operations). If you perform other file system operations with the file handle before requesting an oplock, a deadlock might occur.<br/><br/>**Note:** You can safely call the [CloseHandle](../handleapi/nf-handleapi-closehandle.md) function on the file handle without first requesting an oplock. |
| **FILE_FLAG_OVERLAPPED**<br/>`0x40000000` | The file or device is being opened or created for asynchronous I/O.<br/><br/>When subsequent I/O operations are completed on this handle, the event specified in the [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md) structure will be set to the signaled state.<br/><br/>If this flag is specified, the file can be used for simultaneous read and write operations.<br/><br/>If this flag is not specified, then I/O operations are serialized, even if the calls to the read and write functions specify an [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md) structure.<br/><br/>For information about considerations when using a file handle created with this flag, see the [Synchronous and Asynchronous I/O Handles](#synchronous-and-asynchronous-io-handles) section of this topic. |
| **FILE_FLAG_POSIX_SEMANTICS**<br/>`0x01000000` | Access will occur according to POSIX rules. This includes allowing multiple files with names, differing only in case, for file systems that support that naming. Use care when using this option, because files created with this flag may not be accessible by applications that are written for MS-DOS or 16-bit Windows. |
| **FILE_FLAG_RANDOM_ACCESS**<br/>`0x10000000` | Access is intended to be random. The system can use this as a hint to optimize file caching.<br/><br/>This flag has no effect if the file system does not support cached I/O and **FILE_FLAG_NO_BUFFERING**.<br/><br/>For more information, see the **Caching Behavior** section of this topic. |
| **FILE_FLAG_SESSION_AWARE**<br/>`0x00800000` | The file or device is being opened with session awareness. If this flag is not specified, then per-session devices (such as a device using RemoteFX USB Redirection) cannot be opened by processes running in session 0. This flag has no effect for callers not in session 0. This flag is supported only on server editions of Windows. |
| **FILE_FLAG_SEQUENTIAL_SCAN**<br/>`0x08000000` | Access is intended to be sequential from beginning to end. The system can use this as a hint to optimize file caching.<br/><br/>This flag should not be used if read-behind (that is, backwards scans) will be used.<br/><br/>This flag has no effect if the file system does not support cached I/O and **FILE_FLAG_NO_BUFFERING**.<br/><br/>For more information, see the **Caching Behavior** section of this topic. |
| **FILE_FLAG_WRITE_THROUGH**<br/>`0x80000000` | Write operations will not go through any intermediate cache, they will go directly to disk.<br/><br/>For additional information, see the [Caching Behavior](#caching-behavior) section of this topic. |

### -field dwSecurityQosFlags

The *dwSecurityQosFlags* parameter specifies SQOS information. For more information, see [Impersonation Levels](/windows/win32/SecAuthZ/impersonation-levels).

| Security flag | Meaning |
|---------------|---------|
| **SECURITY_ANONYMOUS** | Impersonates a client at the Anonymous impersonation level. |
| **SECURITY_CONTEXT_TRACKING** | The security tracking mode is dynamic. If this flag is not specified, the security tracking mode is static. |
| **SECURITY_DELEGATION** | Impersonates a client at the Delegation impersonation level. |
| **SECURITY_EFFECTIVE_ONLY** | Only the enabled aspects of the client's security context are available to the server. If you do not specify this flag, all aspects of the client's security context are available.<br/><br/>This allows the client to limit the groups and privileges that a server can use while impersonating the client. |
| **SECURITY_IDENTIFICATION** | Impersonates a client at the Identification impersonation level. |
| **SECURITY_IMPERSONATION** | Impersonate a client at the impersonation level. This is the default behavior if no other flags are specified. |

### -field lpSecurityAttributes

A pointer to a [SECURITY_ATTRIBUTES](../wtypesbase/ns-wtypesbase-security_attributes.md) structure that contains two separate but related data members: an optional security descriptor, and a Boolean value that determines whether the returned handle can be inherited by child processes.

This parameter can be `NULL`.

If this parameter is `NULL`, the handle returned by [CreateFile3](nf-fileapi-createfile3.md) cannot be inherited by any child processes the application may create and the file or device associated with the returned handle gets a default security descriptor.

The **lpSecurityDescriptor** member of the structure specifies a [SECURITY_DESCRIPTOR](../winnt/ns-winnt-security_descriptor.md) for a file or device. If this member is `NULL`, the file or device associated with the returned handle is assigned a default security descriptor.

[CreateFile3](nf-fileapi-createfile3.md) ignores the **lpSecurityDescriptor** member when opening an existing file or device, but continues to use the **bInheritHandle** member.

The **bInheritHandle** member of the structure specifies whether the returned handle can be inherited.

For more information, see the Remarks section of the [CreateFile3](nf-fileapi-createfile3.md) topic.

### -field hTemplateFile

A valid handle to a template file with the **GENERIC_READ** access right. The template file supplies file attributes and extended attributes for the file that is being created.

This parameter can be `NULL`.

When opening an existing file, [CreateFile3](nf-fileapi-createfile3.md) ignores this parameter.

When opening a new encrypted file, the file inherits the discretionary access control list from its parent directory. For additional information, see [File Encryption](/windows/win32/fileio/file-encryption).

## -remarks

To compile an application that uses the **CREATEFILE3_EXTENDED_PARAMETERS** structure, define the **_WIN32_WINNT** macro as `0x0602` or later. For more information, see [Using the Windows Headers](/windows/win32/WinProg/using-the-windows-headers).

#### Caching Behavior

Several of the possible values for the **dwFileFlags** member are used to control or affect how the data associated with the handle is cached by the system. They are:

- **FILE_FLAG_NO_BUFFERING**
- **FILE_FLAG_RANDOM_ACCESS**
- **FILE_FLAG_SEQUENTIAL_SCAN**
- **FILE_FLAG_WRITE_THROUGH**
- **FILE_ATTRIBUTE_TEMPORARY**

If none of these flags is specified, the system uses a default general-purpose caching scheme. Otherwise, the system caching behaves as specified for each flag.

Some of these flags should not be combined. For instance, combining **FILE_FLAG_RANDOM_ACCESS** with **FILE_FLAG_SEQUENTIAL_SCAN** is self-defeating.

Specifying the **FILE_FLAG_SEQUENTIAL_SCAN** flag can increase performance for applications that read large files using sequential access. Performance gains can be even more noticeable for applications that read large files mostly sequentially, but occasionally skip forward over small ranges of bytes. If an application moves the file pointer for random access, optimum caching performance most likely will not occur. However, correct operation is still guaranteed.

The flags **FILE_FLAG_WRITE_THROUGH** and **FILE_FLAG_NO_BUFFERING** are independent and may be combined.

If **FILE_FLAG_WRITE_THROUGH** is used but **FILE_FLAG_NO_BUFFERING** is not also specified, so that system caching is in effect, then the data is written to the system cache but is flushed to disk without delay.

If **FILE_FLAG_WRITE_THROUGH** and **FILE_FLAG_NO_BUFFERING** are both specified, so that system caching is not in effect, then the data is immediately flushed to disk without going through the Windows system cache. The operating system also requests a write-through of the hard disk's local hardware cache to persistent media.

> [!NOTE]
> Not all hard disk hardware supports this write-through capability.

Proper use of the **FILE_FLAG_NO_BUFFERING** flag requires special application considerations. For more information, see [File Buffering](/windows/win32/FileIO/file-buffering).

A write-through request via **FILE_FLAG_WRITE_THROUGH** also causes NTFS to flush any metadata changes, such as a time stamp update or a rename operation, that result from processing the request. For this reason, the **FILE_FLAG_WRITE_THROUGH** flag is often used with the **FILE_FLAG_NO_BUFFERING** flag as a replacement for calling the [FlushFileBuffers](nf-fileapi-flushfilebuffers.md) function after each write, which can cause unnecessary performance penalties. Using these flags together avoids those penalties. For general information about the caching of files and metadata, see [File Caching](/windows/win32/FileIO/file-caching).

When **FILE_FLAG_NO_BUFFERING** is combined with **FILE_FLAG_OVERLAPPED**, the flags give maximum asynchronous performance, because the I/O does not rely on the synchronous operations of the memory manager. However, some I/O operations take more time, because data is not being held in the cache. Also, the file metadata may still be cached (for example, when creating an empty file). To ensure that the metadata is flushed to disk, use the [FlushFileBuffers](nf-fileapi-flushfilebuffers.md) function.

Specifying the **FILE_ATTRIBUTE_TEMPORARY** attribute causes file systems to avoid writing data back to mass storage if sufficient cache memory is available, because an application deletes a temporary file after a handle is closed. In that case, the system can entirely avoid writing the data. Although it does not directly control data caching in the same way as the previously mentioned flags, the **FILE_ATTRIBUTE_TEMPORARY** attribute does tell the system to hold as much as possible in the system cache without writing and therefore may be of concern for certain applications.

#### Synchronous and Asynchronous I/O Handles

[CreateFile3](nf-fileapi-createfile3.md) provides for creating a file or device handle that is either synchronous or asynchronous. A synchronous handle behaves such that I/O function calls using that handle are blocked until they complete, while an asynchronous file handle makes it possible for the system to return immediately from I/O function calls, whether they completed the I/O operation or not. As stated previously, this synchronous versus asynchronous behavior is determined by specifying **FILE_FLAG_OVERLAPPED** within the **dwFileFlags** member of the **CREATEFILE3_EXTENDED_PARAMETERS** structure passed in the *lpCreateExParams* parameter. There are several complexities and potential pitfalls when using asynchronous I/O; for more information, see [Synchronous and Asynchronous I/O](/windows/win32/FileIO/synchronous-and-asynchronous-i-o).

## -see-also

[CreateFile3](nf-fileapi-createfile3.md)

[File Management Structures](/windows/win32/fileio/file-management-structures)
