---
UID: NF:imapi.IDiscMaster.ClearFormatContent
title: IDiscMaster::ClearFormatContent (imapi.h)
description: Clears the contents of an unburned image (the current stash file).
helpviewer_keywords: ["ClearFormatContent","ClearFormatContent method [IMAPI]","ClearFormatContent method [IMAPI]","IDiscMaster interface","IDiscMaster interface [IMAPI]","ClearFormatContent method","IDiscMaster.ClearFormatContent","IDiscMaster::ClearFormatContent","_win32_idiscmaster_clearformatcontent","base.idiscmaster_clearformatcontent","imapi.idiscmaster_clearformatcontent","imapi/IDiscMaster::ClearFormatContent"]
old-location: imapi\idiscmaster_clearformatcontent.htm
tech.root: imapi
ms.assetid: d3c0d850-914b-47ae-b614-a292411e6832
ms.date: 12/05/2018
ms.keywords: ClearFormatContent, ClearFormatContent method [IMAPI], ClearFormatContent method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],ClearFormatContent method, IDiscMaster.ClearFormatContent, IDiscMaster::ClearFormatContent, _win32_idiscmaster_clearformatcontent, base.idiscmaster_clearformatcontent, imapi.idiscmaster_clearformatcontent, imapi/IDiscMaster::ClearFormatContent
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
 - IDiscMaster::ClearFormatContent
 - imapi/IDiscMaster::ClearFormatContent
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
 - IDiscMaster.ClearFormatContent
---

# IDiscMaster::ClearFormatContent


## -description

Clears the contents of an unburned image (the current stash file).



## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

The stash file is an internal structure that is used to stage a disc before recording it to media.


<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">SetActiveDiscRecorder</a> determines if there is an IMAPI multi-session disc in the active drive. If so, IMAPI enters multi-session mode automatically. Using 
<b>ClearFormatContent</b> after multi-session mode had been established causes IMAPI to return to single-session mode. This means that a blank disc is required for a 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">RecordDisc</a> burn.

<div class="alert"><b>Caution</b>  Use care when calling this method. There is no confirmation and no recovery. If an application fills the image file with data, then calls this method, the data is gone.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>
