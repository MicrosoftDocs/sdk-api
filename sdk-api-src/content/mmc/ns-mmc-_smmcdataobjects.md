---
UID: NS:mmc._SMMCDataObjects
title: "_SMMCDataObjects"
author: windows-sdk-content
description: The SMMCDataObjects structure defines the format of the data for the CCF_MULTI_SELECT_SNAPINS clipboard format.
old-location: mmc\smmcdataobjects.htm
old-project: mmc
ms.assetid: 4bbfc32e-b70b-4c47-a7b5-6ec2692d1df4
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: SMMCDataObjects, SMMCDataObjects structure [MMC], _SMMCDataObjects, _slate_smmcdataobjects, mmc.smmcdataobjects, mmc/SMMCDataObjects
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmc.h
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
req.typenames: SMMCDataObjects
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SMMCDataObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SMMCDataObjects structure


## -description


The 
<b>SMMCDataObjects</b> structure defines the format of the data for the 
<a href="https://msdn.microsoft.com/56419e7c-6583-4307-9b47-779914a05813">CCF_MULTI_SELECT_SNAPINS</a> clipboard format. The structure contains the array of pointers to the multiselection data object of each snap-in represented in the set of selected items in the result pane.


## -struct-fields




### -field count

The number of snap-ins whose items are selected in the result pane.


### -field lpDataObject

Array of pointers to the multiselection data objects for each snap-in selected in the result pane.


## -remarks



Each data object consists of the node types associated with a given snap-in. Data objects are passed using 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>.

The multiselection data objects hold a list that contains each node type represented in the set of selected items for that particular snap-in in the result pane. The list of node types from a particular multiselection data object can be retrieved as an array of node type GUIDs by calling <b>IDataObject::GetData</b> on that data object with the 
<a href="https://msdn.microsoft.com/135b3526-e725-47b8-9676-b60a9456846c">CCF_OBJECT_TYPES_IN_MULTI_SELECT</a> clipboard format.

Each multiselection data object also holds a list that contains the selected items owned by a particular snap-in. Each snap-in is responsible for defining the format and method of retrieval of the list of its selected items.




## -see-also




<a href="https://msdn.microsoft.com/56419e7c-6583-4307-9b47-779914a05813">CCF_MULTI_SELECT_SNAPINS</a>



<a href="https://msdn.microsoft.com/9fe5db82-d3b7-4050-b653-6c19cdc21525">Multiselection</a>



<a href="https://msdn.microsoft.com/e17574ea-a6a9-440e-97cf-7b87f13bf21e">SMMCObjectTypes</a>
 

 

