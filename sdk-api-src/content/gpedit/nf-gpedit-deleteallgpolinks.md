---
UID: NF:gpedit.DeleteAllGPOLinks
title: DeleteAllGPOLinks function (gpedit.h)
description: The DeleteAllGPOLinks function deletes all GPO links for the specified site, domain, or organizational unit.
helpviewer_keywords: ["DeleteAllGPOLinks","DeleteAllGPOLinks function [Group Policy]","_win32_deleteallgpolinks","gpedit/DeleteAllGPOLinks","policy.deleteallgpolinks"]
old-location: policy\deleteallgpolinks.htm
tech.root: Policy
ms.assetid: 164b1d10-9ec0-43c8-80fe-be1ad8ec991f
ms.date: 12/05/2018
ms.keywords: DeleteAllGPOLinks, DeleteAllGPOLinks function [Group Policy], _win32_deleteallgpolinks, gpedit/DeleteAllGPOLinks, policy.deleteallgpolinks
req.header: gpedit.h
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
req.lib: Gpedit.lib
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeleteAllGPOLinks
 - gpedit/DeleteAllGPOLinks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gpedit.dll
api_name:
 - DeleteAllGPOLinks
---

# DeleteAllGPOLinks function


## -description

The
    <b>DeleteAllGPOLinks</b> function deletes all GPO links for the specified site, domain, or organizational unit.

## -parameters

### -param lpContainer [in]

A value that specifies the path to the site, domain, or organizational unit, in ADSI format (LDAP://cn=<i>user</i>, ou=<i>users</i>, dc=<i>coname</i>, dc=<i>com</i>). You cannot specify a server name in this parameter.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-creategpolink">CreateGPOLink</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-deletegpolink">DeleteGPOLink</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>