---
UID: NE:appmgmt._INSTALLSPECTYPE
title: INSTALLSPECTYPE (appmgmt.h)
description: The INSTALLSPECTYPE enumeration values define the ways a group policy application can be specified to the InstallApplication function. The values are used in the Type member of INSTALLDATA.
helpviewer_keywords: ["APPNAME","FILEEXT","INSTALLSPECTYPE","INSTALLSPECTYPE enumeration [Group Policy]","appmgmt/APPNAME","appmgmt/FILEEXT","appmgmt/INSTALLSPECTYPE","policy.installspectype_enum"]
old-location: policy\installspectype_enum.htm
tech.root: Policy
ms.assetid: 9e62a22d-cae7-4b3e-9000-71eddb1f3cad
ms.date: 12/05/2018
ms.keywords: APPNAME, FILEEXT, INSTALLSPECTYPE, INSTALLSPECTYPE enumeration [Group Policy], appmgmt/APPNAME, appmgmt/FILEEXT, appmgmt/INSTALLSPECTYPE, policy.installspectype_enum
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
req.typenames: INSTALLSPECTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INSTALLSPECTYPE
 - appmgmt/_INSTALLSPECTYPE
 - INSTALLSPECTYPE
 - appmgmt/INSTALLSPECTYPE
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
 - INSTALLSPECTYPE
---

# INSTALLSPECTYPE enumeration


## -description

The <b>INSTALLSPECTYPE</b> enumeration values define the ways  a group policy application can be specified to the  <a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a> function. The values are used in the <b>Type</b> member of <a href="/windows/desktop/api/appmgmt/ns-appmgmt-installdata">INSTALLDATA</a>.

## -enum-fields

### -field APPNAME

This constant equals 1. The application is specified by its display name and group policy GUID.

### -field FILEEXT

The application is specified by its file name extension, for example, .jpg.

### -field PROGID

### -field COMCLASS

## -see-also

<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>



<a href="/windows/desktop/api/appmgmt/ns-appmgmt-installdata">INSTALLDATA</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-uninstallapplication">UninstallApplication</a>