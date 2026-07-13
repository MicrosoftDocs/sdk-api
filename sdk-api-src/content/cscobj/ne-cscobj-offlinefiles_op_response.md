---
UID: NE:cscobj.tagOFFLINEFILES_OP_RESPONSE
title: OFFLINEFILES_OP_RESPONSE (cscobj.h)
description: Specifies whether to continue, retry, or stop processing items.
helpviewer_keywords: ["OFFLINEFILES_OP_ABORT","OFFLINEFILES_OP_CONTINUE","OFFLINEFILES_OP_RESPONSE","OFFLINEFILES_OP_RESPONSE enumeration [Offline Files]","OFFLINEFILES_OP_RETRY","cscobj/OFFLINEFILES_OP_ABORT","cscobj/OFFLINEFILES_OP_CONTINUE","cscobj/OFFLINEFILES_OP_RESPONSE","cscobj/OFFLINEFILES_OP_RETRY","of.offlinefiles_op_response"]
old-location: of\offlinefiles_op_response.htm
tech.root: of
ms.assetid: a4b16256-7f6a-4e26-8cf2-3ef7c59ac3af
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_OP_ABORT, OFFLINEFILES_OP_CONTINUE, OFFLINEFILES_OP_RESPONSE, OFFLINEFILES_OP_RESPONSE enumeration [Offline Files], OFFLINEFILES_OP_RETRY, cscobj/OFFLINEFILES_OP_ABORT, cscobj/OFFLINEFILES_OP_CONTINUE, cscobj/OFFLINEFILES_OP_RESPONSE, cscobj/OFFLINEFILES_OP_RETRY, of.offlinefiles_op_response
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_OP_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_OP_RESPONSE
 - cscobj/tagOFFLINEFILES_OP_RESPONSE
 - OFFLINEFILES_OP_RESPONSE
 - cscobj/OFFLINEFILES_OP_RESPONSE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_OP_RESPONSE
---

# OFFLINEFILES_OP_RESPONSE enumeration


## -description

Specifies whether to continue, retry, or stop processing items.

## -enum-fields

### -field OFFLINEFILES_OP_CONTINUE:0

Continue processing items.

### -field OFFLINEFILES_OP_RETRY

Repeat processing of this item.

### -field OFFLINEFILES_OP_ABORT

Stop processing now.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessimpleprogress-itembegin">IOfflineFilesSimpleProgress::ItemBegin</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessimpleprogress-itemresult">IOfflineFilesSimpleProgress::ItemResult</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitembegin">IOfflineFilesSyncProgress::SyncItemBegin</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitemresult">IOfflineFilesSyncProgress::SyncItemResult</a>
