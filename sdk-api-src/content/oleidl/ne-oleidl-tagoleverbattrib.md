---
UID: NE:oleidl.tagOLEVERBATTRIB
title: tagOLEVERBATTRIB
author: windows-driver-content
description: Describes the attributes of a specified verb for an object.
old-location: com\oleverbattrib.htm
old-project: com
ms.assetid: 797498ba-5ad6-4476-87d8-de85b30396f4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: OLEVERBATTRIB, OLEVERBATTRIB enumeration [COM], OLEVERBATTRIB_NEVERDIRTIES, OLEVERBATTRIB_ONCONTAINERMENU, _ole_OLEVERBATTRIB, com.oleverbattrib, oleidl/OLEVERBATTRIB, oleidl/OLEVERBATTRIB_NEVERDIRTIES, oleidl/OLEVERBATTRIB_ONCONTAINERMENU, tagOLEVERBATTRIB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIVIEWPROPSW (Unicode) and OLEUIVIEWPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OLEVERBATTRIB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OleIdl.h
api_name:
-	OLEVERBATTRIB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagOLEVERBATTRIB enumeration


## -description


Describes the attributes of a specified verb for an object. 


## -enum-fields




### -field OLEVERBATTRIB_NEVERDIRTIES

Executing this verb will not cause the object to become dirty and is therefore in need of saving to persistent storage.


### -field OLEVERBATTRIB_ONCONTAINERMENU

Indicates a verb that should appear in the container's menu of verbs for this object. OLEIVERB_HIDE, OLEIVERB_SHOW, and OLEIVERB_OPEN never have this value set.



## -remarks



Values are used in the enumerator (which supports the <a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a> interface) that is created by a call to <a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">IOleObject::EnumVerbs</a>. 




## -see-also




<a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a>



<a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">IOleObject::EnumVerbs</a>



<a href="https://msdn.microsoft.com/657e3cc3-67fb-4458-8dad-f2a31df1b631">OLEVERB</a>
 

 

