---
UID: NF:ntdef.InitializeObjectAttributes
title: InitializeObjectAttributes macro (ntdef.h)
description: The InitializeObjectAttributes macro initializes the opaque OBJECT_ATTRIBUTES structure, which specifies the properties of an object handle to routines that open handles.
helpviewer_keywords: ["InitializeObjectAttributes","InitializeObjectAttributes macro [Kernel-Mode Driver Architecture]","k107_f7e00cf9-9598-4835-b51a-3df9e003587e.xml","kernel.initializeobjectattributes","ntdef/InitializeObjectAttributes"]
old-location: kernel\initializeobjectattributes.htm
tech.root: kernel
ms.assetid: ee89a9af-0bdf-476e-b4e3-eb60662e160d
ms.date: 04/30/2018
ms.keywords: InitializeObjectAttributes, InitializeObjectAttributes macro [Kernel-Mode Driver Architecture], k107_f7e00cf9-9598-4835-b51a-3df9e003587e.xml, kernel.initializeobjectattributes, ntdef/InitializeObjectAttributes
req.header: ntdef.h
req.include-header: Wdm.h, Ntddk.h, Ntdef.h
req.target-type: Desktop
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
req.typenames: 
f1_keywords:
 - InitializeObjectAttributes
 - ntdef/InitializeObjectAttributes
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
 - InitializeObjectAttributes
---

# InitializeObjectAttributes macro


## -description

The <b>InitializeObjectAttributes</b> macro initializes the opaque <a href="/windows/win32/api/ntdef/ns-ntdef-_object_attributes">OBJECT_ATTRIBUTES</a> structure, which specifies the properties of an object handle to routines that open handles.

## -parameters

### -param p

A pointer to the [OBJECT_ATTRIBUTES](./ns-ntdef-_object_attributes.md) structure to initialize.

### -param n

A pointer to a Unicode string that contains the name of the object for which a handle is to be opened. This must either be a fully qualified object name, or a relative path name to the object directory specified by the RootDirectory parameter.

### -param a

Specifies one or more of the following flags:

|Flag|Description|
|---|---|
|OBJ_INHERIT |This handle can be inherited by child processes of the current process.|
|OBJ_PERMANENT|This flag only applies to objects that are named within the object manager. By default, such objects are deleted when all open handles to them are closed. If this flag is specified, the object is not deleted when all open handles are closed. Drivers can use ZwMakeTemporaryObject to delete permanent objects.|
|OBJ_EXCLUSIVE|Only a single handle can be open for this object.|
|OBJ_CASE_INSENSITIVE|If this flag is specified, a case-insensitive comparison is used when matching the ObjectName parameter against the names of existing objects. Otherwise, object names are compared using the default system settings.|
|OBJ_OPENIF|If this flag is specified to a routine that creates objects, and that object already exists then the routine should open that object. Otherwise, the routine creating the object returns an NTSTATUS code of STATUS_OBJECT_NAME_COLLISION.|
|OBJ_KERNEL_HANDLE|Specifies that the handle can only be accessed in kernel mode.|
|OBJ_FORCE_ACCESS_CHECK | The routine opening the handle should enforce all access checks for the object, even if the handle is being opened in kernel mode.|

### -param r

A handle to the root object directory for the path name specified in the ObjectName parameter. If ObjectName is a fully qualified object name, RootDirectory is NULL. Use [ZwCreateDirectoryObject](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwcreatedirectoryobject) to obtain a handle to an object directory.

### -param s

Specifies a security descriptor to apply to an object when it is created. This parameter is optional. Drivers can specify NULL to accept the default security for the object. For more information, see the following Remarks section.

## -syntax

```cpp
VOID InitializeObjectAttributes(
  [out]          POBJECT_ATTRIBUTES   p,
  [in]           PUNICODE_STRING      n,
  [in]           ULONG                a,
  [in]           HANDLE               r,
  [in, optional] PSECURITY_DESCRIPTOR s
);
```

## -remarks

<b>InitializeObjectAttributes</b> initializes an <a href="/windows-hardware/drivers/ddi/content/wudfwdm/ns-wudfwdm-_object_attributes">OBJECT_ATTRIBUTES</a> structure that specifies the properties of an object handle to be opened. The caller can then pass a pointer to this structure to a routine that actually opens the handle. 

Driver routines that run in a process context other than that of the system process must set the OBJ_KERNEL_HANDLE flag for the <i>Attributes</i> parameter. This flag restricts the use of a handle opened for that object to processes running only in kernel mode. Otherwise, the handle can be accessed by the process in whose context the driver is running.

Note that <b>InitializeObjectAttributes</b> always sets the <b>SecurityQualityOfService</b> member of <a href="/windows-hardware/drivers/ddi/content/wudfwdm/ns-wudfwdm-_object_attributes">OBJECT_ATTRIBUTES</a> to <b>NULL</b>. Drivers that require a non-<b>NULL</b> value can set <b>SecurityQualityOfService</b> directly.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-excreatecallback">ExCreateCallback</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-iocreatefile">IoCreateFile</a>

<a href="/windows-hardware/drivers/ddi/content/wudfwdm/ns-wudfwdm-_object_attributes">OBJECT_ATTRIBUTES</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-pscreatesystemthread">PsCreateSystemThread</a>

<a href="/windows-hardware/drivers/ddi/content/ntifs/ns-ntifs-_security_descriptor">SECURITY_DESCRIPTOR</a>

[UNICODE_STRING](./ns-ntdef-_unicode_string.md)

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwcreatedirectoryobject">ZwCreateDirectoryObject</a>

<a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-ntcreatefile">ZwCreateFile</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwcreatekey">ZwCreateKey</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwmaketemporaryobject">ZwMakeTemporaryObject</a>

<a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-ntopenfile">ZwOpenFile</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwopenkey">ZwOpenKey</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwopensection">ZwOpenSection</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-zwopensymboliclinkobject">ZwOpenSymbolicLinkObject</a>
