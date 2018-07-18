---
UID: NS:oleidl.tagOLEVERB
title: tagOLEVERB
author: windows-sdk-content
description: Defines a verb that an object supports. The IOleObject::EnumVerbs method creates an enumerator that can enumerate these structures for an object, and supplies a pointer to the enumerator's IEnumOLEVERB.
old-location: com\oleverb.htm
old-project: com
ms.assetid: 657e3cc3-67fb-4458-8dad-f2a31df1b631
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*LPOLEVERB, LPOLEVERB, LPOLEVERB structure pointer [COM], OLEVERB, OLEVERB structure [COM], _ole_OLEVERB, com.oleverb, oleidl/LPOLEVERB, oleidl/OLEVERB, tagOLEVERB"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OLEVERB, *LPOLEVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEVERB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagOLEVERB structure


## -description


Defines a verb that an object supports. The <a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">IOleObject::EnumVerbs</a> method creates an enumerator that can enumerate these structures for an object, and supplies a pointer to the enumerator's <a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a>.


## -struct-fields




### -field lVerb

Integer identifier associated with this verb.


### -field lpszVerbName

Pointer to a string that contains the verb's name.


### -field fuFlags

In Windows, a group of flags taken from the flag constants beginning with MF_ defined in <a href="https://msdn.microsoft.com/library/ms647616(v=VS.85).aspx">AppendMenu</a>. Containers should use these flags in building an object's verb menu. All Flags defined in <b>AppendMenu</b> are supported except for MF_BITMAP, MF_OWNERDRAW, and MF_POPUP.


### -field grfAttribs

Combination of the verb attributes in the <a href="https://msdn.microsoft.com/797498ba-5ad6-4476-87d8-de85b30396f4">OLEVERBATTRIB</a> enumeration.



## -see-also




<a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a>



<a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">IOleObject::EnumVerbs</a>
 

 

