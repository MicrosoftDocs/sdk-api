---
UID: NF:appmgmt.GetManagedApplicationCategories
title: GetManagedApplicationCategories function (appmgmt.h)
description: The GetManagedApplicationCategories function gets a list of application categories for a domain. The list is the same for all users in the domain.
helpviewer_keywords: ["GetManagedApplicationCategories","GetManagedApplicationCategories function [Group Policy]","appmgmt/GetManagedApplicationCategories","policy.getmanagedapplicationcategories"]
old-location: policy\getmanagedapplicationcategories.htm
tech.root: Policy
ms.assetid: 10824852-7810-483a-91b3-2d9cc3d21934
ms.date: 12/05/2018
ms.keywords: GetManagedApplicationCategories, GetManagedApplicationCategories function [Group Policy], appmgmt/GetManagedApplicationCategories, policy.getmanagedapplicationcategories
req.header: appmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetManagedApplicationCategories
 - appmgmt/GetManagedApplicationCategories
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - GetManagedApplicationCategories
---

# GetManagedApplicationCategories function


## -description

The
    <b>GetManagedApplicationCategories</b> function gets a list of application categories for a domain. The list is the same for all users in the domain.

## -parameters

### -param dwReserved [out]

This parameter is reserved. Its value must be 0.

### -param pAppCategory [out]

A <a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfolist">APPCATEGORYINFOLIST</a> structure that contains a list of application categories. This structure must be freed by calling <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>  when the list is no longer required.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

The structure returned by <b>GetManagedApplicationCategories</b> must be freed by calling <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> when the list is no longer required.

## -see-also

<a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfolist">APPCATEGORYINFOLIST</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>