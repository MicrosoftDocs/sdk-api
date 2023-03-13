---
UID: NS:dsclient.DSCLASSCREATIONINFO
title: DSCLASSCREATIONINFO (dsclient.h)
description: Used with the IDsDisplaySpecifier::GetClassCreationInfo method to hold data about the class creation wizard objects for an object class.
helpviewer_keywords: ["*LPDSCLASSCREATIONINFO","DSCCIF_HASWIZARDDIALOG","DSCCIF_HASWIZARDPRIMARYPAGE","DSCLASSCREATIONINFO","DSCLASSCREATIONINFO structure [Active Directory]","LPDSCLASSCREATIONINFO","LPDSCLASSCREATIONINFO structure pointer [Active Directory]","_glines_dsclasscreationinfo","ad.dsclasscreationinfo","dsclient/DSCLASSCREATIONINFO","dsclient/LPDSCLASSCREATIONINFO"]
old-location: ad\dsclasscreationinfo.htm
tech.root: ad
ms.assetid: 5c1551f7-f651-4b87-829a-ec9a07fb0ec2
ms.date: 12/05/2018
ms.keywords: '*LPDSCLASSCREATIONINFO, DSCCIF_HASWIZARDDIALOG, DSCCIF_HASWIZARDPRIMARYPAGE, DSCLASSCREATIONINFO, DSCLASSCREATIONINFO structure [Active Directory], LPDSCLASSCREATIONINFO, LPDSCLASSCREATIONINFO structure pointer [Active Directory], _glines_dsclasscreationinfo, ad.dsclasscreationinfo, dsclient/DSCLASSCREATIONINFO, dsclient/LPDSCLASSCREATIONINFO'
req.header: dsclient.h
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
req.typenames: DSCLASSCREATIONINFO, *LPDSCLASSCREATIONINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDSCLASSCREATIONINFO
 - dsclient/LPDSCLASSCREATIONINFO
 - DSCLASSCREATIONINFO
 - dsclient/DSCLASSCREATIONINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DSCLASSCREATIONINFO
---

# DSCLASSCREATIONINFO structure


## -description

The <b>DSCLASSCREATIONINFO</b> structure is used with the <a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getclasscreationinfo">IDsDisplaySpecifier::GetClassCreationInfo</a> method to hold data about the class creation wizard objects for an object class.

## -struct-fields

### -field dwFlags

Contains a set of flags that indicate which members of this structure contain valid data. This can be a combination of one or more of the following values.



#### DSCCIF_HASWIZARDDIALOG

The <b>clsidWizardDialog</b> member is valid.



#### DSCCIF_HASWIZARDPRIMARYPAGE

The <b>clsidWizardPrimaryPage</b> member is valid.

### -field clsidWizardDialog

Contains the class identifier of the class creation wizard dialog box. This member is not used if <b>dwFlags</b> does not contain <b>DSCCIF_HASWIZARDDIALOG</b>.

### -field clsidWizardPrimaryPage

Contains the class identifier of the primary property page of the class creation wizard. This member is not used if <b>dwFlags</b> does not contain <b>DSCCIF_HASWIZARDPRIMARYPAGE</b>.

### -field cWizardExtensions

Contains the number of elements in the <b>aWizardExtensions</b> array.

### -field aWizardExtensions

Contains an array of the class identifiers of the  property page extensions. <b>cWizardExtensions</b> specifies the number of elements in this array.

## -see-also

<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-getclasscreationinfo">IDsDisplaySpecifier::GetClassCreationInfo</a>

