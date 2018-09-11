---
UID: NE:winbase._PRIORITY_HINT
title: "_PRIORITY_HINT"
author: windows-sdk-content
description: Defines values that are used with the FILE_IO_PRIORITY_HINT_INFO structure to specify the priority hint for a file I/O operation.
old-location: fs\priority_hint.htm
tech.root: fileio
ms.assetid: 768e563a-5ff5-4dd2-8811-0a823c253a31
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IoPriorityHintLow, IoPriorityHintNormal, IoPriorityHintVeryLow, MaximumIoPriorityHintType, PRIORITY_HINT, PRIORITY_HINT enumeration [Files], _PRIORITY_HINT, fs.priority_hint, winbase/IoPriorityHintLow, winbase/IoPriorityHintNormal, winbase/IoPriorityHintVeryLow, winbase/MaximumIoPriorityHintType, winbase/PRIORITY_HINT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winbase.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - PRIORITY_HINT
product: Windows
targetos: Windows
req.typenames: PRIORITY_HINT
req.redist: 
---

# _PRIORITY_HINT enumeration


## -description


Defines values that are used with the <a href="https://msdn.microsoft.com/a142b8fd-b71c-4449-a8c6-fb23715d1576">FILE_IO_PRIORITY_HINT_INFO</a> structure to specify the priority hint for a file I/O operation.


## -enum-fields




### -field IoPriorityHintVeryLow

The lowest possible priority hint level. The system uses this value for background I/O operations.


### -field IoPriorityHintLow

A low-priority hint level.


### -field IoPriorityHintNormal

A normal-priority hint level. This value is the default setting for an I/O operation.


### -field MaximumIoPriorityHintType

This value is used for validation. Supported values are less than this value.


## -see-also




<a href="https://msdn.microsoft.com/a142b8fd-b71c-4449-a8c6-fb23715d1576">FILE_IO_PRIORITY_HINT_INFO</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

