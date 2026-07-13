---
UID: NS:winternl._TEB
title: TEB (winternl.h)
description: The Thread Environment Block (TEB structure) describes the state of a thread.
helpviewer_keywords: ["*PTEB","PTEB","PTEB structure pointer","TEB","TEB structure","base.teb","winternl/PTEB","winternl/TEB"]
old-location: base\teb.htm
tech.root: backup
ms.assetid: fc77fc09-6319-4daa-ac96-1ded661ef800
ms.date: 12/05/2018
ms.keywords: '*PTEB, PTEB, PTEB structure pointer, TEB, TEB structure, base.teb, winternl/PTEB, winternl/TEB'
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TEB, *PTEB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TEB
 - winternl/_TEB
 - PTEB
 - winternl/PTEB
 - TEB
 - winternl/TEB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winternl.h
api_name:
 - TEB
---

# TEB structure


## -description

<p class="CCE_Message">[This structure may be altered in future versions of Windows. Applications should use the alternate functions listed in this topic.]

The Thread Environment Block (TEB) structure describes the state of a thread.

## -struct-fields

### -field Reserved1

Reserved for internal use by the operating system.


### -field ProcessEnvironmentBlock

A pointer to the [PEB](/windows/desktop/api/winternl/ns-winternl-peb) structure that contains information for the process as a whole.


### -field Reserved2

Reserved for internal use by the operating system.


### -field Reserved3

Reserved for internal use by the operating system.

### -field TlsSlots

Data for [Thread Local Storage](/windows/win32/procthread/thread-local-storage). Call the [TlsGetValue](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function to access it.

### -field Reserved4

Reserved for internal use by the operating system.

### -field Reserved5

Reserved for internal use by the operating system.

### -field ReservedForOle

Do not use. Call [CoGetContextToken](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcontexttoken) instead.

### -field Reserved6

Reserved for internal use by the operating system.

### -field TlsExpansionSlots

Additional data for [Thread Local Storage](/windows/win32/procthread/thread-local-storage). Call the [TlsGetValue](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function to access it.

## -remarks

The definition of this structure may change from one version of Windows to the next. Do not assume a maximum size for this structure. To see the members of this structure, refer to [winternal.h](/windows/win32/api/winternl/).

You should not directly access this structure. To access the values of the *TlsSlots* and *TlsExpansionSlots* fields, call [TlsGetValue](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue). To access the value of the *ReservedForOle* field, call [CoGetContextToken](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcontexttoken).

In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0. This can be used to directly access the 32-bit TEB of a WOW64 thread. This might change in later versions of Windows.

<table>
<tr>
<td>Windows Vista</td>
<td>Windows Server 2008</td>
</tr>
<tr>
<td>Windows 7</td>
<td>Windows Server 2008 R2</td>
</tr>
<tr>
<td>Windows 8</td>
<td>Windows Server 2012</td>
</tr>
<tr>
<td>Windows 8.1</td>
<td>Windows Server 2012 R2</td>
</tr>
</table>

## -see-also

[TlsGetValue](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)
