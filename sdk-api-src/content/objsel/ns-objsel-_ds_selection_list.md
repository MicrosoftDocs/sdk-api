---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

