---
UID: NE:mfreadwrite.MF_SOURCE_READER_CONTROL_FLAG
title: MF_SOURCE_READER_CONTROL_FLAG (mfreadwrite.h)
author: windows-sdk-content
description: Contains flags for the IMFSourceReader::ReadSample method.
old-location: mf\mf_source_reader_control_flag.htm
tech.root: medfound
ms.assetid: a6367fea-ceba-4ce4-9a1b-88a40afc3055
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MF_SOURCE_READER_CONTROLF_DRAIN, MF_SOURCE_READER_CONTROL_FLAG, MF_SOURCE_READER_CONTROL_FLAG enumeration [Media Foundation], mf.mf_source_reader_control_flag, mfreadwrite/MF_SOURCE_READER_CONTROLF_DRAIN, mfreadwrite/MF_SOURCE_READER_CONTROL_FLAG
ms.topic: enum
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - mfreadwrite.h
api_name:
 - MF_SOURCE_READER_CONTROL_FLAG
product: Windows
targetos: Windows
req.typenames: MF_SOURCE_READER_CONTROL_FLAG
req.redist: 
ms.custom: 19H1
---

# MF_SOURCE_READER_CONTROL_FLAG enumeration


## -description


Contains flags for the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">IMFSourceReader::ReadSample</a> method.


## -enum-fields




### -field MF_SOURCE_READER_CONTROLF_DRAIN

Retrieve any pending samples, but do not request any more samples from the media source. To get all of the pending samples, call <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">ReadSample</a> with this flag until the method returns a <b>NULL</b> media sample pointer.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a>
 

 

