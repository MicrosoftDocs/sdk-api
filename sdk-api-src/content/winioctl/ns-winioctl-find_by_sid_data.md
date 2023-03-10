---
UID: NS:winioctl.FIND_BY_SID_DATA
title: FIND_BY_SID_DATA
description: Contains data for the FSCTL_FIND_FILES_BY_SID control code.
helpviewer_keywords: ["*PFIND_BY_SID_DATA","FIND_BY_SID_DATA","FIND_BY_SID_DATA structure [Files]","PFIND_BY_SID_DATA","PFIND_BY_SID_DATA structure pointer [Files]","base.find_by_sid_data","fs.find_by_sid_data","winioctl/FIND_BY_SID_DATA","winioctl/PFIND_BY_SID_DATA"]
old-location: fs\find_by_sid_data.htm
tech.root: fs
ms.assetid: fd0294a1-be43-4353-8edc-dff8bf0b0787
ms.date: 12/05/2018
ms.keywords: '*PFIND_BY_SID_DATA, FIND_BY_SID_DATA, FIND_BY_SID_DATA structure [Files], PFIND_BY_SID_DATA, PFIND_BY_SID_DATA structure pointer [Files], base.find_by_sid_data, fs.find_by_sid_data, winioctl/FIND_BY_SID_DATA, winioctl/PFIND_BY_SID_DATA'
req.header: winioctl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FIND_BY_SID_DATA, *PFIND_BY_SID_DATA
req.redist: 
f1_keywords:
 - PFIND_BY_SID_DATA
 - winioctl/PFIND_BY_SID_DATA
 - FIND_BY_SID_DATA
 - winioctl/FIND_BY_SID_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FIND_BY_SID_DATA
---

# FIND_BY_SID_DATA structure


## -description

Contains data for the 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_find_files_by_sid">FSCTL_FIND_FILES_BY_SID</a> control 
   code.

## -struct-fields

### -field Restart

Indicates whether to restart the search. This member should be 1 on first call, so the search will start 
      from the root. For subsequent calls, this member should be zero so the search will resume at the point where it 
      stopped.

### -field Sid

A <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that specifies the desired creator 
      owner.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_find_files_by_sid">FSCTL_FIND_FILES_BY_SID</a>

