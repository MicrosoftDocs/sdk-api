---
UID: NF:winnls.FILEMUIINFO_GET_MAIN_TYPEID
title: FILEMUIINFO_GET_MAIN_TYPEID macro
author: windows-driver-content
description: Gets the main module types array element associated with the type identifier size and offset in a FILEMUIINFO structure. The information is provided in the dwTypeIDMainSize and dwTypeIDMainOffset members of the structure.
old-location: intl\filemuiinfo_get_main_typeid.htm
old-project: Intl
ms.assetid: 0102b364-ffc7-48a0-a7d1-5a64fba6428e
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: FILEMUIINFO_GET_MAIN_TYPEID, FILEMUIINFO_GET_MAIN_TYPEID macro [Internationalization for Windows Applications], _win32_FILEMUIINFO_GET_MAIN_TYPEID, intl.filemuiinfo_get_main_typeid, winnls/FILEMUIINFO_GET_MAIN_TYPEID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnls.h
api_name:
-	FILEMUIINFO_GET_MAIN_TYPEID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FILEMUIINFO_GET_MAIN_TYPEID macro


## -description


Gets the main module types array element associated with the type identifier size and offset in a <a href="https://msdn.microsoft.com/4c757d19-ac66-4ba4-a691-f575f61961be">FILEMUIINFO</a> structure. The information is provided in the <b>dwTypeIDMainSize</b> and <b>dwTypeIDMainOffset</b> members of the structure.


## -parameters




### -param pInfo

Pointer to the <a href="https://msdn.microsoft.com/4c757d19-ac66-4ba4-a691-f575f61961be">FILEMUIINFO</a> structure.


### -param iType

Index of the array element.


## -see-also




<a href="https://msdn.microsoft.com/4c757d19-ac66-4ba4-a691-f575f61961be">FILEMUIINFO</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/d910d922-33f5-48ff-be0a-1ac11a13383a">Multilingual User Interface Macros</a>
 

 

