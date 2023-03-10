---
UID: NF:gpedit.CreateGPOLink
title: CreateGPOLink function (gpedit.h)
description: The CreateGPOLink function creates a link between the specified GPO and the specified site, domain, or organizational unit.
helpviewer_keywords: ["CreateGPOLink","CreateGPOLink function [Group Policy]","_win32_creategpolink","gpedit/CreateGPOLink","policy.creategpolink"]
old-location: policy\creategpolink.htm
tech.root: Policy
ms.assetid: 25d1035d-4ece-4f57-88f2-139f39dbdb86
ms.date: 12/05/2018
ms.keywords: CreateGPOLink, CreateGPOLink function [Group Policy], _win32_creategpolink, gpedit/CreateGPOLink, policy.creategpolink
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
req.lib: GPEdit.lib
req.dll: GPEdit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateGPOLink
 - gpedit/CreateGPOLink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - GPEdit.dll
api_name:
 - CreateGPOLink
---

# CreateGPOLink function


## -description

The <b>CreateGPOLink</b> function creates a link between 
    the specified GPO and the specified site, domain, or organizational unit.

## -parameters

### -param lpGPO [in]

A value that specifies the path to the GPO, in ADSI format 
      ("LDAP://cn=<i>user</i>, ou=<i>users</i>, dc=<i>coname</i>, dc=<i>com</i>"). 
      You cannot specify a server name in this parameter.

### -param lpContainer [in]

A value that specifies the Active Directory path to the site, domain, or organizational unit.

### -param fHighPriority [in]

A value that specifies the link priority. If this parameter is <b>TRUE</b>, the system 
      creates the link as the highest priority. If this parameter is <b>FALSE</b>, the system 
      creates the link as the lowest priority.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns 
       one of the COM error codes defined in the header file WinError.h. Be aware that you should test explicitly for 
       the return value <b>S_OK</b>. Do not use the <b>SUCCEEDED</b> or 
       <b>FAILED</b> macro on the returned <b>HRESULT</b> to determine success or failure of the 
       function.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-deleteallgpolinks">DeleteAllGPOLinks</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-deletegpolink">DeleteGPOLink</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>