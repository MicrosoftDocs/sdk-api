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
f1_keywords:
- gpmgmt/GPMPermissionType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Gpmgmt.h
api_name:
- GPMPermissionType
targetos: Windows
req.typenames: GPMPermissionType
req.redist: 
ms.custom: 19H1
---

# GPMPermissionType enumeration


## -description


GPMPermissionType defines the categories, permissions included in the categories, and the object to which they can be applied.


## -enum-fields




### -field permGPOApply

The trustee can apply the GPO; corresponds to the READ and APPLY Group Policy access rights being set to "Allow" for a user.


### -field permGPORead

The trustee can read the GPO; corresponds to the READ Group Policy access right set to "Allow" for a user.


### -field permGPOEdit

The trustee can read and edit the policy settings for the GPO; corresponds to the READ, WRITE, CREATE CHILD OBJECT, and DELETE CHILD OBJECT Group Policy access rights set to "Allow" for a user.


### -field permGPOEditSecurityAndDelete

The trustee can read, edit and delete the permissions for the GPO; corresponds to the Group Policy access rights specified by <b>permGPOEdit</b> plus the DELETE, MODIFY PERMISSIONS, and MODIFY OWNER access rights set to "Allow" for a user.


### -field permGPOCustom

The trustee has custom permissions for the GPO.


### -field permWMIFilterEdit

The trustee can edit the WMI filter.


### -field permWMIFilterFullControl

The trustee has full control over the WMI filter.


### -field permWMIFilterCustom

The trustee has custom  permissions  for the WMI filter.


### -field permSOMLink

he trustee can link GPOs to the SOM. Applies to sites, domains and OUs.


### -field permSOMLogging

The trustee can generate RSoP logging data for the SOM. Applies to domains and OUs.


### -field permSOMPlanning

The trustee can generate RSoP planning data for the SOM. Applies to domains and OUs.


### -field permSOMWMICreate

The trustee can create WMI filters in the domain. Applies to domains only.


### -field permSOMWMIFullControl

The trustee has full control over all WMI filters in the domain. Applies to domains only.


### -field permSOMGPOCreate

The trustee can create GPOs in the domain. Applies to domains only.


### -field permStarterGPORead

The trustee can read the Starter GPO; corresponds to the READ Group Policy access right set to "Allow" for a user.


### -field permStarterGPOEdit

The trustee can read and edit the administrative template policy settings for the Starter GPO; corresponds to the READ, WRITE, CREATE CHILD OBJECT, and DELETE CHILD OBJECT Group Policy access rights set to "Allow" for a user.


### -field permStarterGPOFullControl

The trustee has full control for the Starter GPO. Applies to domains only.


### -field permStarterGPOCustom

The trustee has custom permissions for the Starter GPO.


### -field permSOMStarterGPOCreate

The trustee can create Starter GPOs in the domain. Applies to domains only.

