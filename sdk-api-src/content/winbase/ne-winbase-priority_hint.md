---
UID: NE:winbase._PRIORITY_HINT
title: PRIORITY_HINT (winbase.h)
author: windows-sdk-content
description: Defines values that are used with the FILE_IO_PRIORITY_HINT_INFO structure to specify the priority hint for a file I/O operation.
old-location: fs\priority_hint.htm
tech.root: FileIO
ms.assetid: 768e563a-5ff5-4dd2-8811-0a823c253a31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IoPriorityHintLow, IoPriorityHintNormal, IoPriorityHintVeryLow, MaximumIoPriorityHintType, PRIORITY_HINT, PRIORITY_HINT enumeration [Files], fs.priority_hint, winbase/IoPriorityHintLow, winbase/IoPriorityHintNormal, winbase/IoPriorityHintVeryLow, winbase/MaximumIoPriorityHintType, winbase/PRIORITY_HINT
ms.topic: enum
f1_keywords:
- winbase/PRIORITY_HINT
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
ms.custom: 19H1
---

# PRIORITY_HINT enumeration


## -description


Defines values that are used with the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-file_io_priority_hint_info">FILE_IO_PRIORITY_HINT_INFO</a> structure to specify the priority hint for a file I/O operation.


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




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-file_io_priority_hint_info">FILE_IO_PRIORITY_HINT_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>
 

 

