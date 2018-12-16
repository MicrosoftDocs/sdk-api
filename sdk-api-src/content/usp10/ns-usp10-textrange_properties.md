---
UID: NS:usp10.textrange_properties
title: TEXTRANGE_PROPERTIES
author: windows-sdk-content
description: Contains a group of OpenType features to apply to a run.
old-location: intl\textrange_properties.htm
tech.root: Intl
ms.assetid: f43a0873-f499-4d66-9fce-57f332c1dc77
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TEXTRANGE_PROPERTIES, TEXTRANGE_PROPERTIES structure [Internationalization for Windows Applications], _win32_TEXTRANGE_PROPERTIES, intl.textrange_properties, usp10/TEXTRANGE_PROPERTIES
ms.topic: struct
req.header: usp10.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - TEXTRANGE_PROPERTIES
product: Windows
targetos: Windows
req.typenames: TEXTRANGE_PROPERTIES
req.redist: Usp10.dll version 1.600 or greater onWindows XP
---

# TEXTRANGE_PROPERTIES structure


## -description



Contains a group of OpenType features to apply to a run.




## -struct-fields




### -field potfRecords

Pointer to an array of <a href="https://msdn.microsoft.com/3f4d76f7-fd50-4a38-973b-329e477e5960">OPENTYPE_FEATURE_RECORD</a> structures containing OpenType features (records) to apply to the characters in a specific range of text in a run.


### -field cotfRecords

 Number of features in the array specified by <b>potfRecords</b>.


## -see-also




<a href="https://msdn.microsoft.com/3f4d76f7-fd50-4a38-973b-329e477e5960">OPENTYPE_FEATURE_RECORD</a>



<a href="https://msdn.microsoft.com/dd456988-ec9d-4e62-a93f-753ac08a18d9">ScriptPlaceOpenType</a>



<a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

