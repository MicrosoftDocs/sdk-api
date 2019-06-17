---
UID: NS:wmcontainer.ASF_MUX_STATISTICS
title: ASF_MUX_STATISTICS (wmcontainer.h)
author: windows-sdk-content
description: Contains statistics about the progress of the ASF multiplexer.
old-location: mf\asf_mux_statistics.htm
tech.root: medfound
ms.assetid: 353ee03d-b706-4a70-9eaf-c14b47b5159a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 353ee03d-b706-4a70-9eaf-c14b47b5159a, ASF_MUX_STATISTICS, ASF_MUX_STATISTICS structure [Media Foundation], mf.asf_mux_statistics, wmcontainer/ASF_MUX_STATISTICS
ms.topic: struct
f1_keywords: ["wmcontainer/ASF_MUX_STATISTICS"]
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - wmcontainer.h
api_name:
 - ASF_MUX_STATISTICS
product: Windows
targetos: Windows
req.typenames: ASF_MUX_STATISTICS
req.redist: 
ms.custom: 19H1
---

# ASF_MUX_STATISTICS structure


## -description



Contains statistics about the progress of the ASF multiplexer.




## -struct-fields




### -field cFramesWritten

Number of frames written by the ASF multiplexer.


### -field cFramesDropped

Number of frames dropped by the ASF multiplexer.


## -remarks



Use <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getstatistics">IMFASFMultiplexer::GetStatistics</a> to retrieve this structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getstatistics">IMFASFMultiplexer::GetStatistics</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

