---
UID: NE:msinkaut.InkPersistenceCompressionMode
title: InkPersistenceCompressionMode (msinkaut.h)
description: Defines values for the compression modes that are used to save the InkDisp object to a serialized format.
old-location: tablet\inkpersistencecompressionmode.htm
tech.root: tablet
ms.assetid: dac49948-3977-4952-a6c0-f54c4a0a2e36
ms.date: 12/05/2018
ms.keywords: IPCM_Default, IPCM_MaximumCompression, IPCM_NoCompression, InkPersistenceCompressionMode, InkPersistenceCompressionMode enumeration [Tablet PC], dac49948-3977-4952-a6c0-f54c4a0a2e36, msinkaut/IPCM_Default, msinkaut/IPCM_MaximumCompression, msinkaut/IPCM_NoCompression, msinkaut/InkPersistenceCompressionMode, tablet.inkpersistencecompressionmode
f1_keywords:
- msinkaut/InkPersistenceCompressionMode
dev_langs:
- c++
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
- msinkaut.h
api_name:
- InkPersistenceCompressionMode
targetos: Windows
req.typenames: InkPersistenceCompressionMode
req.redist: 
ms.custom: 19H1
---

# InkPersistenceCompressionMode enumeration


## -description



Defines values for the compression modes that are used to save the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object to a serialized format.




## -enum-fields




### -field IPCM_Default

The default. Provides the best tradeoff between save-time and storage for the typical application. 


### -field IPCM_MaximumCompression

Maximum compression. This is the default value.


### -field IPCM_NoCompression

No compression. Used when save-time is more important than the amount of storage space used and when compatibility between versions is important.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save">Save Method [InkDisp Class]</a>
 

 

