---
UID: NE:gpmgmt.__MIDL___MIDL_itf_gpmgmt_0000_0000_0002
title: GPMPermissionType (gpmgmt.h)
description: The categories, permissions included in the categories, and the object to which they can be applied.
helpviewer_keywords: ["GPMPermissionType","GPMPermissionType enumeration [GPMC]","gpmc.gpmpermissiontype","gpmgmt/GPMPermissionType","gpmgmt/permGPOApply","gpmgmt/permGPOCustom","gpmgmt/permGPOEdit","gpmgmt/permGPOEditSecurityAndDelete","gpmgmt/permGPORead","gpmgmt/permSOMGPOCreate","gpmgmt/permSOMLink","gpmgmt/permSOMLogging","gpmgmt/permSOMPlanning","gpmgmt/permSOMStarterGPOCreate","gpmgmt/permSOMWMICreate","gpmgmt/permSOMWMIFullControl","gpmgmt/permStarterGPOCustom","gpmgmt/permStarterGPOEdit","gpmgmt/permStarterGPOFullControl","gpmgmt/permStarterGPORead","gpmgmt/permWMIFilterCustom","gpmgmt/permWMIFilterEdit","gpmgmt/permWMIFilterFullControl","permGPOApply","permGPOCustom","permGPOEdit","permGPOEditSecurityAndDelete","permGPORead","permSOMGPOCreate","permSOMLink","permSOMLogging","permSOMPlanning","permSOMStarterGPOCreate","permSOMWMICreate","permSOMWMIFullControl","permStarterGPOCustom","permStarterGPOEdit","permStarterGPOFullControl","permStarterGPORead","permWMIFilterCustom","permWMIFilterEdit","permWMIFilterFullControl"]
old-location: gpmc\gpmpermissiontype.htm
tech.root: gpmc
ms.assetid: e363d91b-f4c1-4ccb-a9bb-94c3f1c5f6aa
ms.date: 12/05/2018
ms.keywords: GPMPermissionType, GPMPermissionType enumeration [GPMC], gpmc.gpmpermissiontype, gpmgmt/GPMPermissionType, gpmgmt/permGPOApply, gpmgmt/permGPOCustom, gpmgmt/permGPOEdit, gpmgmt/permGPOEditSecurityAndDelete, gpmgmt/permGPORead, gpmgmt/permSOMGPOCreate, gpmgmt/permSOMLink, gpmgmt/permSOMLogging, gpmgmt/permSOMPlanning, gpmgmt/permSOMStarterGPOCreate, gpmgmt/permSOMWMICreate, gpmgmt/permSOMWMIFullControl, gpmgmt/permStarterGPOCustom, gpmgmt/permStarterGPOEdit, gpmgmt/permStarterGPOFullControl, gpmgmt/permStarterGPORead, gpmgmt/permWMIFilterCustom, gpmgmt/permWMIFilterEdit, gpmgmt/permWMIFilterFullControl, permGPOApply, permGPOCustom, permGPOEdit, permGPOEditSecurityAndDelete, permGPORead, permSOMGPOCreate, permSOMLink, permSOMLogging, permSOMPlanning, permSOMStarterGPOCreate, permSOMWMICreate, permSOMWMIFullControl, permStarterGPOCustom, permStarterGPOEdit, permStarterGPOFullControl, permStarterGPORead, permWMIFilterCustom, permWMIFilterEdit, permWMIFilterFullControl
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GPMPermissionType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_gpmgmt_0000_0000_0002
 - gpmgmt/__MIDL___MIDL_itf_gpmgmt_0000_0000_0002
 - GPMPermissionType
 - gpmgmt/GPMPermissionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gpmgmt.h
api_name:
 - GPMPermissionType
---

# GPMPermissionType enumeration


## -description

GPMPermissionType defines the categories, permissions included in the categories, and the object to which they can be applied.

## -enum-fields

### -field permGPOApply:0x10000

The trustee can apply the GPO; corresponds to the READ and APPLY Group Policy access rights being set to "Allow" for a user.

### -field permGPORead:0x10100

The trustee can read the GPO; corresponds to the READ Group Policy access right set to "Allow" for a user.

### -field permGPOEdit:0x10101

The trustee can read and edit the policy settings for the GPO; corresponds to the READ, WRITE, CREATE CHILD OBJECT, and DELETE CHILD OBJECT Group Policy access rights set to "Allow" for a user.

### -field permGPOEditSecurityAndDelete:0x10102

The trustee can read, edit and delete the permissions for the GPO; corresponds to the Group Policy access rights specified by <b>permGPOEdit</b> plus the DELETE, MODIFY PERMISSIONS, and MODIFY OWNER access rights set to "Allow" for a user.

### -field permGPOCustom:0x10103

The trustee has custom permissions for the GPO.

### -field permWMIFilterEdit:0x20000

The trustee can edit the WMI filter.

### -field permWMIFilterFullControl:0x20001

The trustee has full control over the WMI filter.

### -field permWMIFilterCustom:0x20002

The trustee has custom  permissions  for the WMI filter.

### -field permSOMLink:0x1c0000

he trustee can link GPOs to the SOM. Applies to sites, domains and OUs.

### -field permSOMLogging:0x180100

The trustee can generate RSoP logging data for the SOM. Applies to domains and OUs.

### -field permSOMPlanning:0x180200

The trustee can generate RSoP planning data for the SOM. Applies to domains and OUs.

### -field permSOMWMICreate:0x100300

The trustee can create WMI filters in the domain. Applies to domains only.

### -field permSOMWMIFullControl:0x100301

The trustee has full control over all WMI filters in the domain. Applies to domains only.

### -field permSOMGPOCreate:0x100400

The trustee can create GPOs in the domain. Applies to domains only.

### -field permStarterGPORead:0x30500

The trustee can read the Starter GPO; corresponds to the READ Group Policy access right set to "Allow" for a user.

### -field permStarterGPOEdit:0x30501

The trustee can read and edit the administrative template policy settings for the Starter GPO; corresponds to the READ, WRITE, CREATE CHILD OBJECT, and DELETE CHILD OBJECT Group Policy access rights set to "Allow" for a user.

### -field permStarterGPOFullControl:0x30502

The trustee has full control for the Starter GPO. Applies to domains only.

### -field permStarterGPOCustom:0x30503

The trustee has custom permissions for the Starter GPO.

### -field permSOMStarterGPOCreate:0x100500

The trustee can create Starter GPOs in the domain. Applies to domains only.

