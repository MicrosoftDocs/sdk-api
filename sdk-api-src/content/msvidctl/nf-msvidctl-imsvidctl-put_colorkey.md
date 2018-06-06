---
UID: NF:msvidctl.IMSVidCtl.put_ColorKey
title: IMSVidCtl::put_ColorKey
author: windows-sdk-content
description: The put_ColorKey method specifies the color key.
old-location: mstv\imsvidctl_put_colorkey.htm
old-project: mstv
ms.assetid: 2896f062-4ff9-4652-89b9-5fe55c6fe472
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_ColorKey method, IMSVidCtl.put_ColorKey, IMSVidCtl::put_ColorKey, IMSVidCtlput_ColorKey, mstv.imsvidctl_put_colorkey, msvidctl/IMSVidCtl::put_ColorKey, put_ColorKey, put_ColorKey method [Microsoft TV Technologies], put_ColorKey method [Microsoft TV Technologies],IMSVidCtl interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.put_ColorKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::put_ColorKey


## -description


The <b>put_ColorKey</b> method specifies the color key.


## -parameters




### -param NewValue [in]

Specifies the color key as an <b>OLE_COLOR</b> value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The color key is used when the video renderer draws to an overlay surface.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/2f197faf-a91e-4984-8858-ceab6506b273">IMSVidCtl::get_ColorKey</a>
 

 

