---
UID: NE:intshcut.translateurl_in_flags
title: TRANSLATEURL_IN_FLAGS (intshcut.h)
description: The TRANSLATEURL_IN_FLAGS enumerated values are used with the TranslateURL function to determine how it will execute.
helpviewer_keywords: ["TRANSLATEURL_FL_GUESS_PROTOCOL","TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL","TRANSLATEURL_IN_FLAGS","TRANSLATEURL_IN_FLAGS enumeration [Windows Shell]","_win32_TRANSLATEURL_IN_FLAGS","intshcut/TRANSLATEURL_FL_GUESS_PROTOCOL","intshcut/TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL","intshcut/TRANSLATEURL_IN_FLAGS","shell.TRANSLATEURL_IN_FLAGS"]
old-location: shell\TRANSLATEURL_IN_FLAGS.htm
tech.root: shell
ms.assetid: b04d5c7d-6d3f-4904-8de5-7586437320e9
ms.date: 12/05/2018
ms.keywords: TRANSLATEURL_FL_GUESS_PROTOCOL, TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL, TRANSLATEURL_IN_FLAGS, TRANSLATEURL_IN_FLAGS enumeration [Windows Shell], _win32_TRANSLATEURL_IN_FLAGS, intshcut/TRANSLATEURL_FL_GUESS_PROTOCOL, intshcut/TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL, intshcut/TRANSLATEURL_IN_FLAGS, shell.TRANSLATEURL_IN_FLAGS
req.header: intshcut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRANSLATEURL_IN_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - translateurl_in_flags
 - intshcut/translateurl_in_flags
 - TRANSLATEURL_IN_FLAGS
 - intshcut/TRANSLATEURL_IN_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intshcut.h
api_name:
 - TRANSLATEURL_IN_FLAGS
---

# TRANSLATEURL_IN_FLAGS enumeration


## -description

The <b>TRANSLATEURL_IN_FLAGS</b> enumerated values are used with the <a href="/windows/desktop/api/intshcut/nf-intshcut-translateurla">TranslateURL</a> function to determine how it will execute.

## -enum-fields

### -field TRANSLATEURL_FL_GUESS_PROTOCOL:0x0001

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <a href="/windows/desktop/api/intshcut/nf-intshcut-translateurla">TranslateURL</a>, the system automatically chooses a scheme and adds it to the URL.

### -field TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL:0x0002

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <a href="/windows/desktop/api/intshcut/nf-intshcut-translateurla">TranslateURL</a>, the system adds the default protocol to the URL.
