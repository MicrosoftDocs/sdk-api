---
UID: NS:commctrl.NMSEARCHWEB
tech.root: Controls
title: NMSEARCHWEB
ms.date: 04/13/2022
targetos: Windows
description: Contains information used to handle an [EN_SEARCHWEB](/windows/win32/controls/en-searchweb) notification code.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: commctrl.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2019 [desktop apps only]
req.target-type: 
req.typenames: NMSEARCHWEB
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - commctrl.h
api_name:
 - NMSEARCHWEB
f1_keywords:
 - NMSEARCHWEB
 - commctrl/NMSEARCHWEB
dev_langs:
 - c++
helpviewer_keywords:
 - NMSEARCHWEB
---

## -description

Contains information used to handle an [EN_SEARCHWEB](/windows/win32/controls/en-searchweb) notification code.

## -struct-fields

### -field hdr

Type: **[NMHDR](/windows/win32/api/winuser/ns-winuser-nmhdr)**

An NMHDR structure that contains additional information about this notification.

### -field entrypoint

Type: **[EC_SEARCHWEB_ENTRYPOINT](ne-commctrl-ec_searchweb_entrypoint.md)**

An enum value that indicates the entry point of the search.

### -field hasQueryText

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

TRUE if there is query text; otherwise, FALSE.

### -field invokeSucceeded

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

TRUE if the invoke succeeded; otherwise, FALSE.

## -remarks

## -see-also

[EN_SEARCHWEB](/windows/win32/controls/en-searchweb)
