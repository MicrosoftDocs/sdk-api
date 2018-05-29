---
UID: NE:objidl.tagSTGTY
title: tagSTGTY
author: windows-sdk-content
description: The STGTY enumeration values are used in the type member of the STATSTG structure to indicate the type of the storage element. A storage element is a storage object, a stream object, or a byte-array object (LOCKBYTES).
old-location: stg\stgty.htm
old-project: Stg
ms.assetid: 67189e7a-b089-4a29-adf8-ad7c459c7974
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: STGTY, STGTY enumeration [Structured Storage], STGTY_LOCKBYTES, STGTY_PROPERTY, STGTY_STORAGE, STGTY_STREAM, _stg_stgty, objidl/STGTY, objidl/STGTY_LOCKBYTES, objidl/STGTY_PROPERTY, objidl/STGTY_STORAGE, objidl/STGTY_STREAM, stg.stgty, tagSTGTY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STGTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Objidl.h
api_name:
-	STGTY
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagSTGTY enumeration


## -description


The 
<b>STGTY</b> enumeration values are used in the <b>type</b> member of the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure to indicate the type of the storage element. A storage element is a storage object, a stream object, or a byte-array object (LOCKBYTES).


## -enum-fields




### -field STGTY_STORAGE

Indicates that the storage element is a storage object.


### -field STGTY_STREAM

Indicates that the storage element is a stream object.


### -field STGTY_LOCKBYTES

Indicates that the storage element is a byte-array object.


### -field STGTY_PROPERTY

Indicates that the storage element is a property storage object.


## -see-also




<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>



<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>
 

 

