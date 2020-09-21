---
UID: NE:accctrl._TRUSTEE_FORM
title: TRUSTEE_FORM (accctrl.h)
description: Values that indicate the type of data pointed to by the ptstrName member of the TRUSTEE structure.
helpviewer_keywords: ["TRUSTEE_BAD_FORM","TRUSTEE_FORM","TRUSTEE_FORM enumeration [Security]","TRUSTEE_IS_NAME","TRUSTEE_IS_OBJECTS_AND_NAME","TRUSTEE_IS_OBJECTS_AND_SID","TRUSTEE_IS_SID","_win32_trustee_form_str","accctrl/TRUSTEE_BAD_FORM","accctrl/TRUSTEE_FORM","accctrl/TRUSTEE_IS_NAME","accctrl/TRUSTEE_IS_OBJECTS_AND_NAME","accctrl/TRUSTEE_IS_OBJECTS_AND_SID","accctrl/TRUSTEE_IS_SID","security.trustee_form"]
old-location: security\trustee_form.htm
tech.root: security
ms.assetid: 991ac6cb-3fc9-4915-b5c9-ae73efb25d68
ms.date: 12/05/2018
ms.keywords: TRUSTEE_BAD_FORM, TRUSTEE_FORM, TRUSTEE_FORM enumeration [Security], TRUSTEE_IS_NAME, TRUSTEE_IS_OBJECTS_AND_NAME, TRUSTEE_IS_OBJECTS_AND_SID, TRUSTEE_IS_SID, _win32_trustee_form_str, accctrl/TRUSTEE_BAD_FORM, accctrl/TRUSTEE_FORM, accctrl/TRUSTEE_IS_NAME, accctrl/TRUSTEE_IS_OBJECTS_AND_NAME, accctrl/TRUSTEE_IS_OBJECTS_AND_SID, accctrl/TRUSTEE_IS_SID, security.trustee_form
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TRUSTEE_FORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTEE_FORM
 - accctrl/_TRUSTEE_FORM
 - TRUSTEE_FORM
 - accctrl/TRUSTEE_FORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - TRUSTEE_FORM
---

# TRUSTEE_FORM enumeration


## -description

The <b>TRUSTEE_FORM</b> enumeration contains values that indicate the type of data pointed to by the <b>ptstrName</b> member of the 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.

## -enum-fields

### -field TRUSTEE_IS_SID

The <b>ptstrName</b> member is a pointer to a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that identifies the trustee.

### -field TRUSTEE_IS_NAME

The <b>ptstrName</b> member is a pointer to a null-terminated string that identifies the trustee.

### -field TRUSTEE_BAD_FORM

Indicates a trustee form that is not valid.

### -field TRUSTEE_IS_OBJECTS_AND_SID

The <b>ptstrName</b> member is a pointer to an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_sid">OBJECTS_AND_SID</a> structure that contains the SID of the trustee and the GUIDs of the object types in an object-specific <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).

### -field TRUSTEE_IS_OBJECTS_AND_NAME

The <b>ptstrName</b> member is a pointer to an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a> structure that contains the name of the trustee and the names of the object types in an object-specific ACE.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_sid">OBJECTS_AND_SID</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>