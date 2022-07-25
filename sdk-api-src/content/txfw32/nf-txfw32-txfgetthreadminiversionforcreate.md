---
UID: NF:txfw32.TxfGetThreadMiniVersionForCreate
title: TxfGetThreadMiniVersionForCreate
description: Returns the MiniVersion a subsequent create is set to open.
tech.root: fs
helpviewer_keywords: ["TxfGetThreadMiniVersionForCreate"]
ms.date: 4/26/2019
ms.keywords: TxfGetThreadMiniVersionForCreate
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: TxfW32.dll
req.header: txfw32.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: TxfW32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - TxfGetThreadMiniVersionForCreate
 - txfw32/TxfGetThreadMiniVersionForCreate
dev_langs:
 - c++
topic_type:
 - apiref
 - kbSyntax
api_type:
 - DllExport
api_location:
 - TxfW32.dll
api_name:
 - TxfGetThreadMiniVersionForCreate
---

## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Returns the MiniVersion a subsequent create is set to open.

## -parameters

### -param MiniVersion

Pointer to a USHORT which will receive the result.

## -remarks

## -see-also
