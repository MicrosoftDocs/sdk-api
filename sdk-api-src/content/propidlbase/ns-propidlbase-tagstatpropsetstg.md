---
UID: NS:propidlbase.tagSTATPROPSETSTG
title: tagSTATPROPSETSTG
author: windows-sdk-content
description: The STATPROPSETSTG structure contains information about a property set.
old-location: stg\statpropsetstg.htm
old-project: Stg
ms.assetid: 8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: STATPROPSETSTG, STATPROPSETSTG structure [Structured Storage], _stg_statpropsetstg, propidlbase/STATPROPSETSTG, stg.statpropsetstg, tagSTATPROPSETSTG
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STATPROPSETSTG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	propidlbase.h
api_name:
-	STATPROPSETSTG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagSTATPROPSETSTG structure


## -description



			The 
<b>STATPROPSETSTG</b> structure contains information about a property set. To get this information, call 
<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>, which fills in a buffer containing the information describing the current property set. To enumerate the 
<b>STATPROPSETSTG</b> structures for the property sets in the current property-set storage, call 
<a href="https://msdn.microsoft.com/979ee86b-fabc-428c-8134-f16c2a33270f">IPropertySetStorage::Enum</a> to get a pointer to an enumerator. You can then call the enumeration methods of the 
<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a> interface on the enumerator. The structure is defined as follows:


## -struct-fields




### -field fmtid

FMTID of the current property set, specified when the property set was initially created.


### -field clsid

<b>CLSID</b> associated with this property set, specified when the property set was initially created and possibly modified thereafter with 
<a href="https://msdn.microsoft.com/88c916e5-b7f0-4f4d-b049-df2b0e1c2423">IPropertyStorage::SetClass</a>. If not set, the value will be <b>CLSID_NULL</b>.


### -field grfFlags

Flag values of the property set, as specified in 
<a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>.


### -field mtime

Time in Universal Coordinated Time (UTC) when the property set was last modified.


### -field ctime

Time in UTC when this property set was created.


### -field atime

Time in UTC when this property set was last accessed.


### -field dwOSVersion

 




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a>



<a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>



<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>
 

 

