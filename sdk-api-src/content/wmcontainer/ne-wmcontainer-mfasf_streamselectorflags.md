---
UID: NE:wmcontainer.MFASF_STREAMSELECTORFLAGS
title: MFASF_STREAMSELECTORFLAGS
author: windows-sdk-content
description: Defines the ASF stream selector options.
old-location: mf\mfasf_streamselector_flags.htm
tech.root: medfound
ms.assetid: 2ececb4a-9516-4066-bf01-0924252f93ee
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 2ececb4a-9516-4066-bf01-0924252f93ee, MFASF_STREAMSELECTORFLAGS, MFASF_STREAMSELECTOR_DISABLE_THINNING, MFASF_STREAMSELECTOR_FLAGS, MFASF_STREAMSELECTOR_FLAGS enumeration [Media Foundation], MFASF_STREAMSELECTOR_USE_AVERAGE_BITRATE, enumeration [Media Foundation], mf.mfasf_streamselector_flags, wmcontainer/MFASF_STREAMSELECTOR_DISABLE_THINNING, wmcontainer/MFASF_STREAMSELECTOR_FLAGS, wmcontainer/MFASF_STREAMSELECTOR_USE_AVERAGE_BITRATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - MFASF_STREAMSELECTOR_FLAGS
product: Windows
targetos: Windows
req.typenames: MFASF_STREAMSELECTOR_FLAGS
req.redist: 
---

# MFASF_STREAMSELECTORFLAGS enumeration


## -description



Defines the ASF stream selector options.




## -enum-fields




### -field MFASF_STREAMSELECTOR_DISABLE_THINNING

The stream selector will not set thinning. Thinning is the process of removing samples from a stream to reduce the bit rate.


### -field MFASF_STREAMSELECTOR_USE_AVERAGE_BITRATE

The stream selector will use the average bit rate of streams when selecting streams.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

