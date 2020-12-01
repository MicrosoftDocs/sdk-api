---
UID: NF:gpedit.DeleteGPOLink
title: DeleteGPOLink function (gpedit.h)
description: The DeleteGPOLink function deletes the link between the specified GPO and the specified site, domain, or organizational unit.
helpviewer_keywords: ["DeleteGPOLink","DeleteGPOLink function [Group Policy]","_win32_deletegpolink","gpedit/DeleteGPOLink","policy.deletegpolink"]
old-location: policy\deletegpolink.htm
tech.root: Policy
ms.assetid: e797bc8d-c0c5-4d93-b553-6c07029af01f
ms.date: 12/05/2018
ms.keywords: DeleteGPOLink, DeleteGPOLink function [Group Policy], _win32_deletegpolink, gpedit/DeleteGPOLink, policy.deletegpolink
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
 - DeleteGPOLink
 - gpedit/DeleteGPOLink
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
 - DeleteGPOLink
---

# DeleteGPOLink function


## -description

The
    <b>DeleteGPOLink</b> function deletes the link between the specified GPO and the specified site, domain, or organizational unit.

## -parameters

### -param lpGPO [in]

A value that specifies the path to the GPO, in ADSI format (LDAP://cn=<i>user</i>, ou=<i>users</i>, dc=<i>coname</i>, dc=<i>com</i>). You cannot specify a server name in this parameter.

### -param lpContainer [in]

Specifies the Active Directory path to the site, domain, or organizational unit.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the  header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-creategpolink">CreateGPOLink</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-deleteallgpolinks">DeleteAllGPOLinks</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>