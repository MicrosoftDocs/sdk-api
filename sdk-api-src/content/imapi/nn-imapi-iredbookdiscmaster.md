---
UID: NN:imapi.IRedbookDiscMaster
title: IRedbookDiscMaster (imapi.h)
description: The IRedbookDiscMaster interface enables the staging of an audio CD image. It represents one of the formats supported by MSDiscMasterObj, and it allows the creation of multi-track audio discs in Track-at-Once mode (fixed-size audio gaps).
helpviewer_keywords: ["IRedbookDiscMaster","IRedbookDiscMaster interface [IMAPI]","IRedbookDiscMaster interface [IMAPI]","described","_win32_iredbookdiscmaster","base.iredbookdiscmaster","imapi.iredbookdiscmaster","imapi/IRedbookDiscMaster"]
old-location: imapi\iredbookdiscmaster.htm
tech.root: imapi
ms.assetid: ea531b22-869a-400e-801f-00bb85ebaac2
ms.date: 12/05/2018
ms.keywords: IRedbookDiscMaster, IRedbookDiscMaster interface [IMAPI], IRedbookDiscMaster interface [IMAPI],described, _win32_iredbookdiscmaster, base.iredbookdiscmaster, imapi.iredbookdiscmaster, imapi/IRedbookDiscMaster
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRedbookDiscMaster
 - imapi/IRedbookDiscMaster
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IRedbookDiscMaster
---

# IRedbookDiscMaster interface


## -description

The 
<b>IRedbookDiscMaster</b> interface enables the staging of an audio CD image. It represents one of the formats supported by <b>MSDiscMasterObj</b>, and it allows the creation of multi-track audio discs in Track-at-Once mode (fixed-size audio gaps).

Tracks are created in the stash file, data is added to them, and then they are closed. Only one track is staged at a time; this is called the <i>open track</i>. The remaining tracks are closed and committed to the image, while the open track has available to it all the blocks that are not in use by closed tracks.

## -inheritance

The <b>IRedbookDiscMaster</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRedbookDiscMaster</b> also has these types of members:

