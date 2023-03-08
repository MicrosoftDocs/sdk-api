---
UID: NN:winsync.ICoreFragment
title: ICoreFragment (winsync.h)
description: Represents knowledge of all items in the scope for a specific set of change units.
helpviewer_keywords: ["ICoreFragment","ICoreFragment interface [Windows Sync]","ICoreFragment interface [Windows Sync]","described","winsync.icorefragment","winsync/ICoreFragment"]
old-location: winsync\icorefragment.htm
tech.root: winsync
ms.assetid: 3e232531-ad44-4ad1-b186-46edbc07291b
ms.date: 12/05/2018
ms.keywords: ICoreFragment, ICoreFragment interface [Windows Sync], ICoreFragment interface [Windows Sync],described, winsync.icorefragment, winsync/ICoreFragment
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
 - ICoreFragment
 - winsync/ICoreFragment
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
 - ICoreFragment
---

# ICoreFragment interface


## -description

Represents knowledge of all items in the scope for a specific set of change units.

## -inheritance

The <b>ICoreFragment</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICoreFragment</b> also has these types of members:

## -remarks

An <b>ISyncKnowledge2</b> object contains one or more <b>ICoreFragment</b> objects, each of which contains knowledge that applies to a specific set of change units. Typically, one of the <b>ICoreFragment</b> objects contains no change unit IDs. The knowledge that is contained in the <b>ICoreFragment</b> object that contains no change unit IDs applies to all change unit IDs that are not otherwise contained in another <b>ICoreFragment</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
