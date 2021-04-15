---
UID: NS:wtypesbase._SECURITY_ATTRIBUTES
tech.root: com
title: SECURITY_ATTRIBUTES
ms.date: 03/23/2021
targetos: Windows
description: The SECURITY_ATTRIBUTES structure contains the security descriptor for an object and specifies whether the handle retrieved by specifying this structure is inheritable.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wtypesbase.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.target-type: 
req.typenames: SECURITY_ATTRIBUTES, *PSECURITY_ATTRIBUTES, *LPSECURITY_ATTRIBUTES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - _SECURITY_ATTRIBUTES
 - PSECURITY_ATTRIBUTES
 - SECURITY_ATTRIBUTES
f1_keywords:
 - _SECURITY_ATTRIBUTES
 - wtypesbase/_SECURITY_ATTRIBUTES
 - PSECURITY_ATTRIBUTES
 - wtypesbase/PSECURITY_ATTRIBUTES
 - SECURITY_ATTRIBUTES
 - wtypesbase/SECURITY_ATTRIBUTES
dev_langs:
 - c++
---

## -description

The **SECURITY\_ATTRIBUTES** structure contains the [*security descriptor*](../winnt/ns-winnt-security_descriptor.md) for an object and specifies whether the handle retrieved by specifying this structure is inheritable. This structure provides security settings for objects created by various functions, such as [**CreateFile**](../fileapi/nf-fileapi-createfilew.md), [**CreatePipe**](../namedpipeapi/nf-namedpipeapi-createpipe.md), [**CreateProcess**](../processthreadsapi/nf-processthreadsapi-createprocessa.md), [**RegCreateKeyEx**](../winreg/nf-winreg-regcreatekeyexw.md), or [**RegSaveKeyEx**](../winreg/nf-winreg-regsavekeyexa.md).


## -struct-fields

### -field nLength

The size, in bytes, of this structure. Set this value to the size of the **SECURITY\_ATTRIBUTES** structure.

### -field lpSecurityDescriptor

A pointer to a [**SECURITY\_DESCRIPTOR**](../winnt/ns-winnt-security_descriptor.md) structure that controls access to the object. If the value of this member is **NULL**, the object is assigned the default security descriptor associated with the [*access token*](/windows/win32/secauthz/access-tokens) of the calling process. This is not the same as granting access to everyone by assigning a **NULL** [*discretionary access control list*](/windows/win32/secauthz/dacls-and-aces) (DACL). By default, the default DACL in the access token of a process allows access only to the user represented by the access token.
    
For information about creating a security descriptor, see [Creating a Security Descriptor](/windows/win32/secauthz/creating-a-security-descriptor-for-a-new-object-in-c--).


### -field bInheritHandle

A Boolean value that specifies whether the returned handle is inherited when a new process is created. If this member is **TRUE**, the new process inherits the handle.


## -remarks

## -see-also

