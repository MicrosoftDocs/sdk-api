---
UID: NE:cscobj.tagOFFLINEFILES_OP_RESPONSE
title: tagOFFLINEFILES_OP_RESPONSE
author: windows-sdk-content
description: Specifies whether to continue, retry, or stop processing items.
old-location: of\offlinefiles_op_response.htm
tech.root: OfflineFiles
ms.assetid: a4b16256-7f6a-4e26-8cf2-3ef7c59ac3af
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: OFFLINEFILES_OP_ABORT, OFFLINEFILES_OP_CONTINUE, OFFLINEFILES_OP_RESPONSE, OFFLINEFILES_OP_RESPONSE enumeration [Offline Files], OFFLINEFILES_OP_RETRY, cscobj/OFFLINEFILES_OP_ABORT, cscobj/OFFLINEFILES_OP_CONTINUE, cscobj/OFFLINEFILES_OP_RESPONSE, cscobj/OFFLINEFILES_OP_RETRY, of.offlinefiles_op_response, tagOFFLINEFILES_OP_RESPONSE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_OP_RESPONSE
product: Windows
targetos: Windows
req.typenames: OFFLINEFILES_OP_RESPONSE
req.redist: 
---

# tagOFFLINEFILES_OP_RESPONSE enumeration


## -description


Specifies whether to continue, retry, or stop processing items.


## -enum-fields




### -field OFFLINEFILES_OP_CONTINUE

Continue processing items.


### -field OFFLINEFILES_OP_RETRY

Repeat processing of this item.


### -field OFFLINEFILES_OP_ABORT

Stop processing now.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530617(v=VS.85).aspx">IOfflineFilesSimpleProgress::ItemBegin</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530618(v=VS.85).aspx">IOfflineFilesSimpleProgress::ItemResult</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530638(v=VS.85).aspx">IOfflineFilesSyncProgress::SyncItemBegin</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530639(v=VS.85).aspx">IOfflineFilesSyncProgress::SyncItemResult</a>
 

 

