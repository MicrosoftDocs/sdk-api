---
UID: NS:ntdef._OBJECT_ATTRIBUTES
title: _OBJECT_ATTRIBUTES (ntdef.h)
description: The OBJECT_ATTRIBUTES structure specifies attributes that can be applied to objects or object handles by routines that create objects and/or return handles.
helpviewer_keywords: ["*POBJECT_ATTRIBUTES","OBJECT_ATTRIBUTES","OBJECT_ATTRIBUTES structure [Kernel-Mode Driver Architecture]","POBJECT_ATTRIBUTES","POBJECT_ATTRIBUTES structure pointer [Kernel-Mode Driver Architecture]","_OBJECT_ATTRIBUTES","kernel.object_attributes","kstruct_c_62b87332-0ef4-4c45-8c4f-0fc12d18582b.xml","ntdef/OBJECT_ATTRIBUTES","ntdef/POBJECT_ATTRIBUTES"]
old-location: kernel\object_attributes.htm
tech.root: kernel
ms.assetid: 08f5a141-abce-4890-867c-5fe8c4239905
ms.date: 08/09/2023
ms.keywords: '*POBJECT_ATTRIBUTES, OBJECT_ATTRIBUTES, OBJECT_ATTRIBUTES structure [Kernel-Mode Driver Architecture], POBJECT_ATTRIBUTES, POBJECT_ATTRIBUTES structure pointer [Kernel-Mode Driver Architecture], _OBJECT_ATTRIBUTES, kernel.object_attributes, kstruct_c_62b87332-0ef4-4c45-8c4f-0fc12d18582b.xml, ntdef/OBJECT_ATTRIBUTES, ntdef/POBJECT_ATTRIBUTES'
req.header: ntdef.h
req.include-header: D3dkmthk.h, Ntdef.h, Wdm.h, Ntddk.h, Ntifs.h, Fltkernel.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: OBJECT_ATTRIBUTES
f1_keywords:
 - _OBJECT_ATTRIBUTES
 - ntdef/_OBJECT_ATTRIBUTES
 - OBJECT_ATTRIBUTES
 - ntdef/OBJECT_ATTRIBUTES
 - ntdef/ANSI_STRING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntdef.h
api_name:
 - OBJECT_ATTRIBUTES
---

# _OBJECT_ATTRIBUTES structure

## -description

The **OBJECT_ATTRIBUTES** structure specifies attributes that can be applied to objects or object handles by routines that create objects and/or return handles to objects.

## -struct-fields

### -field Length

The number of bytes of data contained in this structure. The [InitializeObjectAttributes](nf-ntdef-initializeobjectattributes.md) macro sets this member to **sizeof**(**OBJECT_ATTRIBUTES**).

### -field RootDirectory

Optional handle to the root object directory for the path name specified by the *ObjectName* member. If *RootDirectory* is `NULL`, *ObjectName* must point to a fully qualified object name that includes the full path to the target object. If *RootDirectory* is non-`NULL`, *ObjectName* specifies an object name relative to the *RootDirectory* directory. The *RootDirectory* handle can refer to a file system directory or an object directory in the object manager namespace.

### -field ObjectName

Pointer to a [Unicode string](ns-ntdef-_unicode_string.md) that contains the name of the object for which a handle is to be opened. This must either be a fully qualified object name, or a relative path name to the directory specified by the *RootDirectory* member.

### -field Attributes

Bitmask of flags that specify object handle attributes. This member can contain one or more of the flags in the following table.

| Flag | Meaning |
|------|---------|
| OBJ_INHERIT | This handle can be inherited by child processes of the current process. |
| OBJ_PERMANENT | This flag only applies to objects that are named within the object manager. By default, such objects are deleted when all open handles to them are closed. If this flag is specified, the object is not deleted when all open handles are closed. Drivers can use the [ZwMakeTemporaryObject](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwmaketemporaryobject) routine to make a permanent object non-permanent. |
| OBJ_EXCLUSIVE | If this flag is set and the **OBJECT_ATTRIBUTES** structure is passed to a routine that creates an object, the object can be accessed exclusively. That is, once a process opens such a handle to the object, no other processes can open handles to this object.<br/><br/>If this flag is set and the **OBJECT_ATTRIBUTES** structure is passed to a routine that creates an object handle, the caller is requesting exclusive access to the object for the process context that the handle was created in. This request can be granted only if the **OBJ_EXCLUSIVE** flag was set when the object was created.
| OBJ_CASE_INSENSITIVE | If this flag is specified, a case-insensitive comparison is used when matching the name pointed to by the **ObjectName** member against the names of existing objects. Otherwise, object names are compared using the default system settings. |
| OBJ_OPENIF | If this flag is specified, by using the object handle, to a routine that creates objects and if that object already exists, the routine should open that object. Otherwise, the routine creating the object returns an NTSTATUS code of **STATUS_OBJECT_NAME_COLLISION**. |
| OBJ_OPENLINK | If an object handle, with this flag set, is passed to a routine that opens objects and if the object is a symbolic link object, the routine should open the symbolic link object itself, rather than the object that the symbolic link refers to (which is the default behavior). |
| OBJ_KERNEL_HANDLE | The handle is created in system process context and can only be accessed from kernel mode. |
| OBJ_FORCE_ACCESS_CHECK | The routine that opens the handle should enforce all access checks for the object, even if the handle is being opened in kernel mode. |
| OBJ_DONT_REPARSE | If this flag is set, no reparse points will be followed when parsing the name of the associated object. If any reparses are encountered the attempt will fail and return an **STATUS_REPARSE_POINT_ENCOUNTERED** result. This can be used to determine if there are any reparse points in the object's path, in security scenarios. |
| OBJ_IGNORE_IMPERSONATED_DEVICEMAP | A device map is a mapping between DOS device names and devices in the system, and is used when resolving DOS names. Separate device maps exists for each user in the system, and users can manage their own device maps. Typically during impersonation, the impersonated user's device map would be used. However, when this flag is set, the process user's device map is used instead. |
| OBJ_VALID_ATTRIBUTES | Reserved. |

### -field SecurityDescriptor

Specifies a security descriptor ([SECURITY_DESCRIPTOR](/windows-hardware/drivers/ddi/content/ntifs/ns-ntifs-_security_descriptor)) for the object when the object is created. If *SecurityDescriptor* is `NULL`, the object will receive default security settings. See [DACL for a New Object](/windows/win32/secauthz/dacl-for-a-new-object).

### -field SecurityQualityOfService

Optional quality of service to be applied to the object when it is created. Used to indicate the security impersonation level and context tracking mode (dynamic or static). Currently, the [InitializeObjectAttributes](nf-ntdef-initializeobjectattributes.md) macro sets this member to `NULL`.

## -remarks

Use the [InitializeObjectAttributes](nf-ntdef-initializeobjectattributes.md) macro to initialize the members of the **OBJECT_ATTRIBUTES** structure. Note that **InitializeObjectAttributes** initializes the *SecurityQualityOfService* member to `NULL`. If you must specify a non-`NULL` value, set the *SecurityQualityOfService* member after initialization.

To apply the attributes contained in this structure to an object or object handle, pass a pointer to this structure to a routine that accesses objects or returns object handles, such as [ZwCreateFile](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-ntcreatefile) or [ZwCreateDirectoryObject](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwcreatedirectoryobject).

All members of this structure are read-only. If a member of this structure is a pointer, the object that this member points to is read-only as well. Read-only members and objects can be used to acquire relevant information but must not be modified. To set the members of this structure, use the **InitializeObjectAttributes** macro.

Driver routines that run in a process context other than that of the system process must set the **OBJ_KERNEL_HANDLE** flag for the *Attributes* member (by using the **InitializeObjectAttributes** macro). This restricts the use of a handle opened for that object to processes running only in kernel mode. Otherwise, the handle can be accessed by the process in whose context the driver is running.

## -see-also

[FltCreateCommunicationPort](/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatecommunicationport)

[FltCreateFile](/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatefile)

[FltCreateFileEx](/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatefileex)

[FltCreateFileEx2](/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatefileex2)

[InitializeObjectAttributes](nf-ntdef-initializeobjectattributes.md)

[IoCreateFile](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-iocreatefile)

[IoCreateFileEx](/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-iocreatefileex)

[IoCreateFileSpecifyDeviceObjectHint](/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-iocreatefilespecifydeviceobjecthint)

[ZwCreateDirectoryObject](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwcreatedirectoryobject)

[ZwCreateFile](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-ntcreatefile)

[DACL for a New Object](/windows/win32/secauthz/dacl-for-a-new-object)
