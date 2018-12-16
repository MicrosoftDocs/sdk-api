---
UID: NE:accctrl._TRUSTEE_FORM
title: TRUSTEE_FORM
author: windows-sdk-content
description: Values that indicate the type of data pointed to by the ptstrName member of the TRUSTEE structure.
old-location: security\trustee_form.htm
tech.root: secauthz
ms.assetid: 991ac6cb-3fc9-4915-b5c9-ae73efb25d68
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TRUSTEE_BAD_FORM, TRUSTEE_FORM, TRUSTEE_FORM enumeration [Security], TRUSTEE_IS_NAME, TRUSTEE_IS_OBJECTS_AND_NAME, TRUSTEE_IS_OBJECTS_AND_SID, TRUSTEE_IS_SID, _win32_trustee_form_str, accctrl/TRUSTEE_BAD_FORM, accctrl/TRUSTEE_FORM, accctrl/TRUSTEE_IS_NAME, accctrl/TRUSTEE_IS_OBJECTS_AND_NAME, accctrl/TRUSTEE_IS_OBJECTS_AND_SID, accctrl/TRUSTEE_IS_SID, security.trustee_form
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - TRUSTEE_FORM
product: Windows
targetos: Windows
req.typenames: TRUSTEE_FORM
req.redist: 
---

# TRUSTEE_FORM enumeration


## -description


The <b>TRUSTEE_FORM</b> enumeration contains values that indicate the type of data pointed to by the <b>ptstrName</b> member of the 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -enum-fields




### -field TRUSTEE_IS_SID

The <b>ptstrName</b> member is a pointer to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) that identifies the trustee.


### -field TRUSTEE_IS_NAME

The <b>ptstrName</b> member is a pointer to a null-terminated string that identifies the trustee.


### -field TRUSTEE_BAD_FORM

Indicates a trustee form that is not valid.


### -field TRUSTEE_IS_OBJECTS_AND_SID

The <b>ptstrName</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/77ba8a3c-01e5-4a3e-835f-c7b9ef60035a">OBJECTS_AND_SID</a> structure that contains the SID of the trustee and the GUIDs of the object types in an object-specific <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE). 


### -field TRUSTEE_IS_OBJECTS_AND_NAME

The <b>ptstrName</b> member is a pointer to an 
<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a> structure that contains the name of the trustee and the names of the object types in an object-specific ACE.


## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a>



<a href="https://msdn.microsoft.com/77ba8a3c-01e5-4a3e-835f-c7b9ef60035a">OBJECTS_AND_SID</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

