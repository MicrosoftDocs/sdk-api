---
UID: NF:winternl.NtQueryObject
title: NtQueryObject function (winternl.h)
description: Retrieves various kinds of object information.
helpviewer_keywords: ["NtQueryObject","NtQueryObject function [Windows API]","winprog.ntqueryobject","winternl/NtQueryObject"]
old-location: winprog\ntqueryobject.htm
tech.root: winprog
ms.assetid: 08c801b5-a315-413e-adc5-576e6a740465
ms.date: 12/05/2018
ms.keywords: NtQueryObject, NtQueryObject function [Windows API], winprog.ntqueryobject, winternl/NtQueryObject
req.header: winternl.h
req.include-header: 
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtQueryObject
 - winternl/NtQueryObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtQueryObject
---

# NtQueryObject function


## -description

<p class="CCE_Message">[This function may be changed or removed from Windows without further notice.]

Retrieves various kinds of object information.

## -parameters

### -param Handle [in, optional]

The handle of the object for which information is being queried.

### -param ObjectInformationClass [in]

One of the following values, as enumerated in <b>OBJECT_INFORMATION_CLASS</b>, indicating the kind of object information to be retrieved.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="ObjectBasicInformation"></a><a id="objectbasicinformation"></a><a id="OBJECTBASICINFORMATION"></a>ObjectBasicInformation

</td>
<td width="60%">
Returns a <b>PUBLIC_OBJECT_BASIC_INFORMATION</b> structure as shown in the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<a id="ObjectTypeInformation"></a><a id="objecttypeinformation"></a><a id="OBJECTTYPEINFORMATION"></a>ObjectTypeInformation

</td>
<td width="60%">
Returns a <b>PUBLIC_OBJECT_TYPE_INFORMATION</b> structure as shown in the following Remarks section.

</td>
</tr>
</table>

### -param ObjectInformation [out, optional]

An optional pointer to a buffer where the requested information is to be returned. The size and structure of this information varies depending on the value of the <i>ObjectInformationClass</i> parameter.

### -param ObjectInformationLength [in]

The size of the buffer pointed to by the <i>ObjectInformation</i> parameter, in bytes.

### -param ReturnLength [out, optional]

An optional pointer to a location where the function writes the actual size of the information requested. If that size is less than or equal to the <i>ObjectInformationLength</i> parameter, the function copies the information into the <i>ObjectInformation</i> buffer; otherwise, it returns an NTSTATUS error code and returns in <i>ReturnLength</i> the size of the buffer required to receive the requested information.

## -returns

Returns an NTSTATUS or error code.

The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.

## -remarks

This function has no associated header file or import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to dynamically link to Ntdll.dll.

If the <i>ObjectInformationClass</i> parameter is <b>ObjectBasicInformation</b>, the information is contained in the following structure.


``` syntax
typedef struct _PUBLIC_OBJECT_BASIC_INFORMATION {
    ULONG Attributes;
    ACCESS_MASK GrantedAccess;
    ULONG HandleCount;
    ULONG PointerCount;
    ULONG Reserved[10];    // reserved for internal use
 } PUBLIC_OBJECT_BASIC_INFORMATION, *PPUBLIC_OBJECT_BASIC_INFORMATION;

```

Available members for this structure include object attributes for the handle (<b>Attributes</b>), the access granted for the handle (<b>GrantedAccess</b>), the number of open handles to the object (<b>HandleCount</b>), and the number of kernel references to the object (<b>PointerCount</b>).

If the <i>ObjectInformationClass</i> parameter is <b>ObjectTypeInformation</b>, the information is contained in the following structure.


``` syntax
typedef struct __PUBLIC_OBJECT_TYPE_INFORMATION {
    UNICODE_STRING TypeName;
    ULONG Reserved [22];    // reserved for internal use
} PUBLIC_OBJECT_TYPE_INFORMATION, *PPUBLIC_OBJECT_TYPE_INFORMATION;

```

The only available member of this structure is the object-type name string (<b>TypeName</b>).
