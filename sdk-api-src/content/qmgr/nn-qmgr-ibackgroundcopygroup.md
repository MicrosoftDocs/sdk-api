---
UID: NN:qmgr.IBackgroundCopyGroup
title: IBackgroundCopyGroup (qmgr.h)
description: Use the IBackgroundCopyGroup interface to manage a group. A group contains download jobs. For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.
helpviewer_keywords: ["IBackgroundCopyGroup","IBackgroundCopyGroup interface [BITS]","IBackgroundCopyGroup interface [BITS]","described","bits.ibackgroundcopygroup","qmgr/IBackgroundCopyGroup"]
old-location: bits\ibackgroundcopygroup.htm
tech.root: Bits
ms.assetid: 51ddd89a-489a-4b83-ad45-838809a6d2e8
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyGroup, IBackgroundCopyGroup interface [BITS], IBackgroundCopyGroup interface [BITS],described, bits.ibackgroundcopygroup, qmgr/IBackgroundCopyGroup
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyGroup
 - qmgr/IBackgroundCopyGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup
 - IBackgroundCopyGroup.InternalSetProp
 - IBackgroundCopyGroup.QueryNewJobInterface
 - IBackgroundCopyGroup.SetNotificationPointer
---

# IBackgroundCopyGroup interface


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>IBackgroundCopyGroup</b> interface to manage a group. A group contains download jobs. For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.

## -inheritance

The <b>IBackgroundCopyGroup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyGroup</b> also has these types of members:

