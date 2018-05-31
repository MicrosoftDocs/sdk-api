---
UID: NE:objidl.tagDATADIR
title: tagDATADIR
author: windows-sdk-content
description: Specifies the direction of the data flow. This determines the formats that the resulting enumerator can enumerate.
old-location: com\datadir.htm
old-project: com
ms.assetid: 395d7511-f491-4d6c-9360-cae7e16e8524
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DATADIR, DATADIR enumeration [COM], DATADIR_GET, DATADIR_SET, _ole_DATADIR, com.datadir, objidl/DATADIR, objidl/DATADIR_GET, objidl/DATADIR_SET, tagDATADIR
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
req.typenames: DATADIR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ObjIdl.h
api_name:
-	DATADIR
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagDATADIR enumeration


## -description


Specifies the direction of the data flow. This determines the formats that the resulting enumerator can enumerate.


## -enum-fields




### -field DATADIR_GET

Requests that <a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a> supply an enumerator for the formats that can be specified in<a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. 


### -field DATADIR_SET

Requests that <a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a> supply an enumerator for the formats that can be specified in <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a>. 



## -see-also




<a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a>



<a href="https://msdn.microsoft.com/6caebc68-a136-40f2-92d8-7f8003c18e5c">OleRegEnumFormatEtc</a>
 

 

