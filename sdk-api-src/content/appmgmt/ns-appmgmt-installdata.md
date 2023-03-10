---
UID: NS:appmgmt._INSTALLDATA
title: INSTALLDATA (appmgmt.h)
description: The INSTALLDATA structure specifies a group-policy application to be installed by InstallApplication.
helpviewer_keywords: ["*PINSTALLDATA","INSTALLDATA","INSTALLDATA structure [Group Policy]","PINSTALLDATA","PINSTALLDATA structure pointer [Group Policy]","appmgmt/INSTALLDATA","appmgmt/PINSTALLDATA","policy.installdata_str"]
old-location: policy\installdata_str.htm
tech.root: Policy
ms.assetid: 0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c
ms.date: 12/05/2018
ms.keywords: '*PINSTALLDATA, INSTALLDATA, INSTALLDATA structure [Group Policy], PINSTALLDATA, PINSTALLDATA structure pointer [Group Policy], appmgmt/INSTALLDATA, appmgmt/PINSTALLDATA, policy.installdata_str'
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
req.typenames: INSTALLDATA, *PINSTALLDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INSTALLDATA
 - appmgmt/_INSTALLDATA
 - PINSTALLDATA
 - appmgmt/PINSTALLDATA
 - INSTALLDATA
 - appmgmt/INSTALLDATA
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
 - INSTALLDATA
---

# INSTALLDATA structure


## -description

The <b>INSTALLDATA</b> structure specifies a group-policy application to  be installed by <a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a>.

## -struct-fields

### -field Type

Defines  how <b>Spec</b> specifies the application to <a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a>.     <b>Type</b> can be  one of the <a href="/windows/desktop/api/appmgmt/ne-appmgmt-installspectype">INSTALLSPECTYPE</a> enumeration values. Set <b>Type</b> to APPNAME to install an application specified by its user-friendly name and GPO GUID. Set <b>Type</b> to FILEEXT to install  an application specified by its file name extension.

### -field Spec

An <a href="/windows/desktop/api/appmgmt/ns-appmgmt-installspec">INSTALLSPEC</a> structure that specifies the application.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>



<a href="/windows/desktop/api/appmgmt/ns-appmgmt-installspec">INSTALLSPEC</a>



<a href="/windows/desktop/api/appmgmt/ne-appmgmt-installspectype">INSTALLSPECTYPE</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-uninstallapplication">UninstallApplication</a>