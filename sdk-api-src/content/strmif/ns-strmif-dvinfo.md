---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

