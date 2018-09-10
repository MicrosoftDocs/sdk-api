---
UID: NS:strmif.DVINFO
title: DVINFO
author: windows-sdk-content
description: The DVINFO structure describes the format of a digital video (DV) stream.
old-location: dshow\dvinfo.htm
tech.root: DirectShow
ms.assetid: 285a56fc-9c25-4c5a-ae6a-146c17b00e84
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PDVINFO, DVINFO, DVINFO structure [DirectShow], DVINFOStructure, PDVINFO, PDVINFO structure pointer [DirectShow], dshow.dvinfo, strmif/DVINFO, strmif/PDVINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - strmif.h
api_name:
 - DVINFO
product: Windows
targetos: Windows
req.typenames: DVINFO, *PDVINFO
req.redist: 
---

# DVINFO structure


## -description



The <b>DVINFO</b> structure describes the format of a digital video (DV) stream.




## -struct-fields




### -field dwDVAAuxSrc

Specifies the audio auxiliary (AAUX) source pack for the first audio block.
          


### -field dwDVAAuxCtl

Specifies the AAUX source control Pack for the first audio block.
          


### -field dwDVAAuxSrc1

Specifies the AAUX source pack for the second audio block.
          


### -field dwDVAAuxCtl1

Specifies the AAUX source control pack for the second audio block.
          


### -field dwDVVAuxSrc

Specifies the video auxiliary (VAUX) source pack.
          


### -field dwDVVAuxCtl

Specifies the VAUX source control pack.
          


### -field dwDVReserved

Reserved. Set this array to zero.
          


## -remarks



The AAUX and VAUX packs are defined in IEC 61834-4.




## -see-also




<a href="https://msdn.microsoft.com/ae1ec184-afc3-4ec1-9b92-f53656293446">DV Data in the AVI File Format</a>



<a href="https://msdn.microsoft.com/f0723da5-4f53-4f83-a657-ae42815a784e">DVINFO Field Settings in the MSDV Driver</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

