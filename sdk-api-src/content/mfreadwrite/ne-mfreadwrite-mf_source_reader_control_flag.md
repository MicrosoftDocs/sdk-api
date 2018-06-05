---
UID: NE:mfreadwrite.MF_SOURCE_READER_CONTROL_FLAG
title: MF_SOURCE_READER_CONTROL_FLAG
author: windows-sdk-content
description: Contains flags for the IMFSourceReader::ReadSample method.
old-location: mf\mf_source_reader_control_flag.htm
old-project: medfound
ms.assetid: a6367fea-ceba-4ce4-9a1b-88a40afc3055
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MF_SOURCE_READER_CONTROLF_DRAIN, MF_SOURCE_READER_CONTROL_FLAG, MF_SOURCE_READER_CONTROL_FLAG enumeration [Media Foundation], mf.mf_source_reader_control_flag, mfreadwrite/MF_SOURCE_READER_CONTROLF_DRAIN, mfreadwrite/MF_SOURCE_READER_CONTROL_FLAG
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_SOURCE_READER_CONTROL_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfreadwrite.h
api_name:
-	MF_SOURCE_READER_CONTROL_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MF_SOURCE_READER_CONTROL_FLAG enumeration


## -description


Contains flags for the <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a> method.


## -enum-fields




### -field MF_SOURCE_READER_CONTROLF_DRAIN

Retrieve any pending samples, but do not request any more samples from the media source. To get all of the pending samples, call <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">ReadSample</a> with this flag until the method returns a <b>NULL</b> media sample pointer.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

