---
UID: NN:winsync.ISyncChangeWithPrerequisite
title: ISyncChangeWithPrerequisite (winsync.h)
description: Represents metadata about a change that is based on the prerequisite knowledge that is associated with the change.
helpviewer_keywords: ["ISyncChangeWithPrerequisite","ISyncChangeWithPrerequisite interface [Windows Sync]","ISyncChangeWithPrerequisite interface [Windows Sync]","described","winsync.isyncchangewithprerequisite","winsync/ISyncChangeWithPrerequisite"]
old-location: winsync\isyncchangewithprerequisite.htm
tech.root: winsync
ms.assetid: 7650fc2c-fe2d-4cb1-a22a-433c90c5cb8d
ms.date: 12/05/2018
ms.keywords: ISyncChangeWithPrerequisite, ISyncChangeWithPrerequisite interface [Windows Sync], ISyncChangeWithPrerequisite interface [Windows Sync],described, winsync.isyncchangewithprerequisite, winsync/ISyncChangeWithPrerequisite
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncChangeWithPrerequisite
 - winsync/ISyncChangeWithPrerequisite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeWithPrerequisite
---

# ISyncChangeWithPrerequisite interface


## -description

Represents metadata about a change that is based on the prerequisite knowledge that is associated with the change.

## -inheritance

The <b>ISyncChangeWithPrerequisite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChangeWithPrerequisite</b> also has these types of members:

## -remarks

An <b>ISyncChangeWithPrerequisite</b> object can be obtained by passing <b>IID_ ISyncChangeWithPrerequisite</b> to the <b>QueryInterface</b> method of an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
