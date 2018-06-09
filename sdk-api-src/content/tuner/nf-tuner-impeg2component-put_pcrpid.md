---
UID: NF:tuner.IMPEG2Component.put_PCRPID
title: IMPEG2Component::put_PCRPID
author: windows-sdk-content
description: The put_PCRPID method sets the packet identifier (PID) for the packets that contain the PCR for this substream.
old-location: mstv\impeg2component_put_pcrpid.htm
old-project: mstv
ms.assetid: cfe55ec9-cf07-40c5-98da-cb23393490d0
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMPEG2Component interface [Microsoft TV Technologies],put_PCRPID method, IMPEG2Component.put_PCRPID, IMPEG2Component::put_PCRPID, IMPEG2Componentput_PCRPID, mstv.impeg2component_put_pcrpid, put_PCRPID, put_PCRPID method [Microsoft TV Technologies], put_PCRPID method [Microsoft TV Technologies],IMPEG2Component interface, tuner/IMPEG2Component::put_PCRPID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IMPEG2Component.put_PCRPID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMPEG2Component::put_PCRPID


## -description



The <b>put_PCRPID</b> method sets the packet identifier (PID) for the packets that contain the PCR for this substream.




## -parameters




### -param PCRPID [in]

Specifies the PCR PID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/63d1ae17-8e38-457e-98d7-e81e7576f1c1">IMPEG2Component Interface</a>
 

 

