---
UID: NF:securitybaseapi.GetAppContainerAce
tech.root: security
title: GetAppContainerAce (securitybaseapi.h)
ms.date: 12/02/2022
ms.keywords: GetAppContainerAce
targetos: Windows
description: Retrieves a value that indicates whether a package or capability SID is present.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Advapi32.dll
req.header: securitybaseapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Advapi32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - api-ms-win-security-base-l1-2-1.dll
 - api-ms-win-security-base-l1-2-0.dll
 - securitybaseapi.h
api_name:
 - GetAppContainerAce
f1_keywords:
 - GetAppContainerAce
 - securitybaseapi/GetAppContainerAce
dev_langs:
 - c++
helpviewer_keywords:
 - GetAppContainerAce
---

# GetAppContainerAce function (securitybaseapi.h)

## -description

Retrieves a value that indicates whether a package or capability SID is present.

## -parameters

### -param Acl [in]

A pointer to an [ACL](/windows/desktop/api/winnt/ns-winnt-acl) structure.

### -param StartingAceIndex [in]

Specifies the position in the ACL's list of ACEs at which to add new ACEs. A value of zero inserts the ACEs at the beginning of the list. A value of MAXDWORD appends the ACEs to the end of the list.

### -param AppContainerAce [out]

Pointer to an AppContainerAce object.

### -param AppContainerAceIndex [out, optional]

The position in the ACL's list of ACEs.

## -returns

If the function succeeds, it returns **TRUE**.

If the function fails, it returns **FALSE**. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** may return one of the error codes defined in WinError.h.

## -remarks

## -see-also
