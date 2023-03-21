---
UID: NE:winbase._PRIORITY_HINT
title: PRIORITY_HINT (winbase.h)
description: Defines values that are used with the FILE_IO_PRIORITY_HINT_INFO structure to specify the priority hint for a file I/O operation.
helpviewer_keywords: ["IoPriorityHintLow","IoPriorityHintNormal","IoPriorityHintVeryLow","MaximumIoPriorityHintType","PRIORITY_HINT","PRIORITY_HINT enumeration [Files]","fs.priority_hint","winbase/IoPriorityHintLow","winbase/IoPriorityHintNormal","winbase/IoPriorityHintVeryLow","winbase/MaximumIoPriorityHintType","winbase/PRIORITY_HINT"]
old-location: fs\priority_hint.htm
tech.root: fs
ms.assetid: 768e563a-5ff5-4dd2-8811-0a823c253a31
ms.date: 12/05/2018
ms.keywords: IoPriorityHintLow, IoPriorityHintNormal, IoPriorityHintVeryLow, MaximumIoPriorityHintType, PRIORITY_HINT, PRIORITY_HINT enumeration [Files], fs.priority_hint, winbase/IoPriorityHintLow, winbase/IoPriorityHintNormal, winbase/IoPriorityHintVeryLow, winbase/MaximumIoPriorityHintType, winbase/PRIORITY_HINT
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
targetos: Windows
req.typenames: PRIORITY_HINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PRIORITY_HINT
 - winbase/_PRIORITY_HINT
 - PRIORITY_HINT
 - winbase/PRIORITY_HINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - PRIORITY_HINT
---

# PRIORITY_HINT enumeration


## -description

Defines values that are used with the <a href="/windows/desktop/api/winbase/ns-winbase-file_io_priority_hint_info">FILE_IO_PRIORITY_HINT_INFO</a> structure to specify the priority hint for a file I/O operation.

## -enum-fields

### -field IoPriorityHintVeryLow:0

The lowest possible priority hint level. The system uses this value for background I/O operations.

### -field IoPriorityHintLow

A low-priority hint level.

### -field IoPriorityHintNormal

A normal-priority hint level. This value is the default setting for an I/O operation.

### -field MaximumIoPriorityHintType

This value is used for validation. Supported values are less than this value.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-file_io_priority_hint_info">FILE_IO_PRIORITY_HINT_INFO</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>
