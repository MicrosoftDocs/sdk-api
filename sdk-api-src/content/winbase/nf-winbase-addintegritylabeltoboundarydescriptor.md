---
UID: NF:winbase.AddIntegrityLabelToBoundaryDescriptor
title: AddIntegrityLabelToBoundaryDescriptor function (winbase.h)
description: Adds a new required security identifier (SID) to the specified boundary descriptor.
helpviewer_keywords: ["AddIntegrityLabelToBoundaryDescriptor","AddIntegrityLabelToBoundaryDescriptor function","base.addintegritylabeltoboundarydescriptor","winbase/AddIntegrityLabelToBoundaryDescriptor"]
old-location: base\addintegritylabeltoboundarydescriptor.htm
tech.root: backup
ms.assetid: 6b56e664-7795-4e30-8bca-1e4df2764606
ms.date: 12/05/2018
ms.keywords: AddIntegrityLabelToBoundaryDescriptor, AddIntegrityLabelToBoundaryDescriptor function, base.addintegritylabeltoboundarydescriptor, winbase/AddIntegrityLabelToBoundaryDescriptor
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddIntegrityLabelToBoundaryDescriptor
 - winbase/AddIntegrityLabelToBoundaryDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
api_name:
 - AddIntegrityLabelToBoundaryDescriptor
---

# AddIntegrityLabelToBoundaryDescriptor function


## -description

Adds a new required security identifier (SID) to the specified boundary descriptor.

## -parameters

### -param BoundaryDescriptor [in, out]

A handle to the boundary descriptor. The <a href="/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a> function returns this handle.

### -param IntegrityLabel [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that represents the mandatory integrity level for the namespace. Use one of the following RID values to create the SID:

<b>SECURITY_MANDATORY_UNTRUSTED_RID</b>
<b>SECURITY_MANDATORY_LOW_RID</b>
<b>SECURITY_MANDATORY_MEDIUM_RID</b>
<b>SECURITY_MANDATORY_SYSTEM_RID</b>
<b>SECURITY_MANDATORY_PROTECTED_PROCESS_RID</b>
For more information, see <a href="/windows/desktop/SecAuthZ/well-known-sids">Well-Known SIDs</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A process can create a private namespace only with an integrity level that is  equal to or lower than the  current integrity level of the process. Therefore, a high integrity-level process can create a high, medium or low integrity-level namespace. A medium integrity-level process can create only a medium or low integrity-level namespace.

A process would usually specify a namespace at the same integrity level as the process for protection against squatting attacks by lower integrity-level processes. 

The security descriptor that the creator places on the namespace determines who can open the namespace. So a low or medium integrity-level process could be given permission to open a high integrity level namespace if the security descriptor of the namespace permits it.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0601 or later.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createboundarydescriptora">CreateBoundaryDescriptor</a>