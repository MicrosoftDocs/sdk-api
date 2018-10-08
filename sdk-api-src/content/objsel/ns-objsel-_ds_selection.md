---
UID: NS:objsel._DS_SELECTION
title: "_DS_SELECTION"
author: windows-sdk-content
description: The DS_SELECTION structure contains data about an object the user selected from an object picker dialog box. The DS_SELECTION_LIST structure contains an array of DS_SELECTION structures.
old-location: ad\ds_selection.htm
tech.root: ad
ms.assetid: 7a587997-0423-450f-a845-bddf12b69fae
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PDS_SELECTION, DS_SELECTION, DS_SELECTION structure [Active Directory], PDS_SELECTION, PDS_SELECTION structure pointer [Active Directory], _DS_SELECTION, _glines_ds_selection, ad.ds__selection, ad.ds_selection, objsel/DS_SELECTION, objsel/PDS_SELECTION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objsel.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objsel.h
api_name:
 - DS_SELECTION
product: Windows
targetos: Windows
req.typenames: DS_SELECTION, *PDS_SELECTION
req.redist: 
---

# _DS_SELECTION structure


## -description


The <b>DS_SELECTION</b> structure contains data about an object the user selected from an object picker dialog box. The 
<a href="https://msdn.microsoft.com/15493b8c-014e-4e69-9e67-40b24d44606d">DS_SELECTION_LIST</a> structure contains an array of <b>DS_SELECTION</b> structures.


## -struct-fields




### -field pwzName

Pointer to a null-terminated Unicode string that contains the object's relative distinguished name (RDN).


### -field pwzADsPath

Pointer to a null-terminated Unicode string that contains the object's ADsPath. The format of this string depends on the flags specified in the <b>flScope</b> member of the 
<a href="https://msdn.microsoft.com/6262b520-1eee-48e0-b3af-636b66d78b3d">DSOP_SCOPE_INIT_INFO</a> structure for the scope from which this object was selected.


### -field pwzClass

Pointer to a null-terminated Unicode string that contains the value of the object's objectClass attribute.


### -field pwzUPN

Pointer to a null-terminated Unicode string that contains the object's userPrincipalName attribute value. If the object does not have a userPrincipalName value, <b>pwzUPN</b> points to an empty string (L"").


### -field pvarFetchedAttributes

Pointer to an array of 
<a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structures. Each <b>VARIANT</b> contains the value of an attribute of the selected object. The attributes retrieved are determined by the attribute names specified in the <b>apwzAttributeNames</b> member of the 
<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a> structure passed to the 
<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a> method. The order of attributes in the <b>pvarFetchedAttributes</b> array corresponds to the order of attribute names specified in the <b>apwzAttributeNames</b> array.

The object picker dialog box may not be able to retrieve the requested attributes. If the attribute cannot be retrieved, the <b>vt</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure contains <b>VT_EMPTY</b>.


### -field flScopeType

Contains one, or more, of the <b>DSOP_SCOPE_TYPE_*</b> that indicate the type of  scope from which this object was selected.  For more information, and a list of <b>DSOP_SCOPE_TYPE_*</b> flags, see the <b>flType</b> member of the 
<a href="https://msdn.microsoft.com/6262b520-1eee-48e0-b3af-636b66d78b3d">DSOP_SCOPE_INIT_INFO</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a>



<a href="https://msdn.microsoft.com/6262b520-1eee-48e0-b3af-636b66d78b3d">DSOP_SCOPE_INIT_INFO</a>



<a href="https://msdn.microsoft.com/15493b8c-014e-4e69-9e67-40b24d44606d">DS_SELECTION_LIST</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a>
 

 

