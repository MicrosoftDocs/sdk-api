---
UID: NS:objsel._DS_SELECTION_LIST
title: "_DS_SELECTION_LIST"
author: windows-sdk-content
description: The DS_SELECTION_LIST structure contains data about the objects the user selected from an object picker dialog box.
old-location: ad\ds_selection_list.htm
old-project: AD
ms.assetid: 15493b8c-014e-4e69-9e67-40b24d44606d
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PDS_SELECTION_LIST, DS_SELECTION_LIST, DS_SELECTION_LIST structure [Active Directory], PDS_SELECTION_LIST, PDS_SELECTION_LIST structure pointer [Active Directory], _DS_SELECTION_LIST, _glines_ds_selection_list, ad.ds__selection__list, ad.ds_selection_list, objsel/DS_SELECTION_LIST, objsel/PDS_SELECTION_LIST"
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
tech.root: 
req.typenames: DS_SELECTION_LIST, *PDS_SELECTION_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Objsel.h
api_name:
-	DS_SELECTION_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _DS_SELECTION_LIST structure


## -description


The <b>DS_SELECTION_LIST</b> structure contains data about the objects the user selected from an object picker dialog box. This structure is supplied by the <a href="_ole_idataobject">IDataObject</a> interface supplied by the <a href="https://msdn.microsoft.com/76192a35-10e1-46e3-8724-7637d47d8eca">IDsObjectPicker::InvokeDialog</a> method in the <a href="https://msdn.microsoft.com/cd634e3b-0eb7-4144-b9e1-1d27a322f72c">CFSTR_DSOP_DS_SELECTION_LIST</a> data format.




## -struct-fields




### -field cItems

Contains the number of elements in the <b>aDsSelection</b> array.


### -field cFetchedAttributes

Contains the number of elements returned in the <b>pvarFetchedAttributes</b> member of each 
<a href="https://msdn.microsoft.com/7a587997-0423-450f-a845-bddf12b69fae">DS_SELECTION</a> structure.


### -field aDsSelection

Contains an array of <a href="https://msdn.microsoft.com/7a587997-0423-450f-a845-bddf12b69fae">DS_SELECTION</a> structures, one for each object selected by the user. The <b>cItems</b> member indicates the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/cd634e3b-0eb7-4144-b9e1-1d27a322f72c">CFSTR_DSOP_DS_SELECTION_LIST</a>



<a href="https://msdn.microsoft.com/7a587997-0423-450f-a845-bddf12b69fae">DS_SELECTION</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/76192a35-10e1-46e3-8724-7637d47d8eca">IDsObjectPicker::InvokeDialog</a>
 

 

