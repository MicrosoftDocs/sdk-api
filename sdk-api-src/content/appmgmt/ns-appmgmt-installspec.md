---
UID: NS:appmgmt._INSTALLSPEC
title: INSTALLSPEC (appmgmt.h)
description: The INSTALLSPEC structure specifies a group policy application by its user-friendly name and group policy GUID or by its file name extension. The Spec member of the INSTALLDATA structure provides this information to the InstallApplication function.
helpviewer_keywords: ["INSTALLSPEC","INSTALLSPEC union [Group Policy]","appmgmt/INSTALLSPEC","policy.installspec_union"]
old-location: policy\installspec_union.htm
tech.root: Policy
ms.assetid: e9c1b943-9cb0-480f-8ab7-0f439087216a
ms.date: 12/05/2018
ms.keywords: INSTALLSPEC, INSTALLSPEC union [Group Policy], appmgmt/INSTALLSPEC, policy.installspec_union
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INSTALLSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INSTALLSPEC
 - appmgmt/_INSTALLSPEC
 - INSTALLSPEC
 - appmgmt/INSTALLSPEC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Appmgmt.h
api_name:
 - INSTALLSPEC
---

## -description

The <b>INSTALLSPEC</b> structure specifies a group policy application by its user-friendly name and group policy GUID or by its file name extension. The <b>Spec</b> member of the <a href="/windows/desktop/api/appmgmt/ns-appmgmt-installdata">INSTALLDATA</a>  structure provides this information to the <a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a> function.

## -struct-fields

### -field AppName

Structure that contains the following members.

### -field AppName.Name

The user-friendly name of the application as it appears in <b>Add or Remove Programs</b> and the <a href="/previous-versions/windows/desktop/Policy/group-policy-object-editor">Group Policy Object Editor</a>. You can obtain the name by calling <a href="/windows/desktop/api/appmgmt/nf-appmgmt-getmanagedapplications">GetManagedApplications</a>.

### -field AppName.GPOId

The <b>GUID</b> for the group policy object in which the application exists. You can obtain the group policy object <b>GUID</b> by calling <a href="/windows/desktop/api/appmgmt/nf-appmgmt-getmanagedapplications">GetManagedApplications</a>.

### -field FileExt

The file name extension, such as .jpg,  of the application to be installed.

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a> fails if the <b>Type</b> member of <a href="/windows/desktop/api/appmgmt/ns-appmgmt-installdata">INSTALLDATA</a> equals <b>FILEEXT</b> and there is no application deployed to the user with this file name extension.</div>
<div> </div>

### -field ProgId

This parameter is reserved and should not be used.

### -field COMClass

This parameter is reserved and should not be used.

### -field COMClass.Clsid

This parameter is reserved and should not be used.

### -field COMClass.ClsCtx

This parameter is reserved and should not be used.

## -see-also

<a href="/windows/desktop/api/appmgmt/nf-appmgmt-getmanagedapplications">GetManagedApplications</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>



<a href="/windows/desktop/api/appmgmt/ns-appmgmt-installdata">INSTALLDATA</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-uninstallapplication">UninstallApplication</a>