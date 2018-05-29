---
UID: NF:winnt.IsReparseTagMicrosoft
title: IsReparseTagMicrosoft macro
author: windows-sdk-content
description: Determines whether a reparse point tag indicates a Microsoft reparse point.
old-location: fs\isreparsetagmicrosoft.htm
old-project: FileIO
ms.assetid: f64378a7-084e-41c7-9331-dcffa11e0ae9
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IsReparseTagMicrosoft, IsReparseTagMicrosoft macro [Files], _win32_isreparsetagmicrosoft, base.isreparsetagmicrosoft, fs.isreparsetagmicrosoft, winnt/IsReparseTagMicrosoft
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	IsReparseTagMicrosoft
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IsReparseTagMicrosoft macro


## -description


Determines whether a reparse point tag indicates a Microsoft reparse point.


## -parameters




### -param _tag

The reparse point tag to be tested.


## -remarks



If the Microsoft tag bit is set, Microsoft provides the tag. All other tags must use zero for this bit.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544836">FSCTL_GET_REPARSE_POINT</a>



<a href="https://msdn.microsoft.com/3abb3a08-9a00-43eb-9792-82eab1a25f06">Reparse Points</a>
 

 

