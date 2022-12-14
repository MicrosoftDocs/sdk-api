---
UID: NE:commctrl.EC_ENDOFLINE
title: EC_ENDOFLINE (commctrl.h)
description: Indicates the end of line character used by an edit control.
helpviewer_keywords: ["EC_ENDOFLINE","EC_ENDOFLINE enumeration [Windows Controls]","EC_ENDOFLINE_CR","EC_ENDOFLINE_CRLF","EC_ENDOFLINE_DETECTFROMCONTENT","EC_ENDOFLINE_LF","commctrl/EC_ENDOFLINE","commctrl/EC_ENDOFLINE_CR","commctrl/EC_ENDOFLINE_CRLF","commctrl/EC_ENDOFLINE_DETECTFROMCONTENT","commctrl/EC_ENDOFLINE_LF","controls.ec_endofline"]
old-location: controls\ec_endofline.htm
tech.root: Controls
ms.assetid: 8F84EFE4-E562-46D4-AEC8-2782C9EC31F7
ms.date: 12/05/2018
ms.keywords: EC_ENDOFLINE, EC_ENDOFLINE enumeration [Windows Controls], EC_ENDOFLINE_CR, EC_ENDOFLINE_CRLF, EC_ENDOFLINE_DETECTFROMCONTENT, EC_ENDOFLINE_LF, commctrl/EC_ENDOFLINE, commctrl/EC_ENDOFLINE_CR, commctrl/EC_ENDOFLINE_CRLF, commctrl/EC_ENDOFLINE_DETECTFROMCONTENT, commctrl/EC_ENDOFLINE_LF, controls.ec_endofline
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: EC_ENDOFLINE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EC_ENDOFLINE
 - commctrl/EC_ENDOFLINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - EC_ENDOFLINE
---

# EC_ENDOFLINE enumeration


## -description



Indicates the end of line character used by an edit control.

## -enum-fields

### -field EC_ENDOFLINE_DETECTFROMCONTENT:0

End of line character specified in content.

### -field EC_ENDOFLINE_CRLF:1

End of line character is CRLF.

### -field EC_ENDOFLINE_CR:2

End of line character is CR.

### -field EC_ENDOFLINE_LF:3

End of line character is LF.

## -see-also

<a href="/windows/desktop/controls/em-getendofline">EM_GETENDOFLINE</a>



<a href="/windows/desktop/controls/em-setendofline">EM_SETENDOFLINE</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-edit_getendofline">Edit_GetEndOfLine</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-edit_setendofline">Edit_SetEndOfLine</a>
