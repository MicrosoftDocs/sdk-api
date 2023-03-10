---
UID: NF:txfw32.TxfSetThreadMiniVersionForCreate
title: TxfSetThreadMiniVersionForCreate
description: Sets the MiniVersion that a subsequent create should open.
tech.root: fs
helpviewer_keywords: ["TxfSetThreadMiniVersionForCreate"]
ms.date: 4/26/2019
ms.keywords: TxfSetThreadMiniVersionForCreate
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
 - TxfSetThreadMiniVersionForCreate
 - txfw32/TxfSetThreadMiniVersionForCreate
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
 - TxfSetThreadMiniVersionForCreate
---

## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Sets the MiniVersion that a subsequent create should open.  It should be returned to its previous state after calling create.  Therefore, prior
to calling this routine, the caller should invoke [TxfGetThreadMiniVersionForCreate](nf-txfw32-txfgetthreadminiversionforcreate.md).

## -parameters

### -param MiniVersion

A USHORT identifying which version should be opened by create.

## -remarks

## -see-also
