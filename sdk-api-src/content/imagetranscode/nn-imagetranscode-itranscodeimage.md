---
UID: NN:imagetranscode.ITranscodeImage
title: ITranscodeImage (imagetranscode.h)

description: Exposes a method that allows conversion to JPEG or bitmap (BMP) image formats from any image type supported by Windows.
old-location: shell\ITranscodeImage.htm
tech.root: shell
ms.assetid: 747a7d5b-df7c-498b-a541-13c6561cebfe

ms.date: 12/05/2018
ms.keywords: ITranscodeImage, ITranscodeImage interface [Windows Shell], ITranscodeImage interface [Windows Shell],described, _shell_ITranscodeImage, imagetranscode/ITranscodeImage, shell.ITranscodeImage
ms.topic: interface
f1_keywords: 
 - "imagetranscode/ITranscodeImage"
dev_langs:
 - c++
req.header: imagetranscode.h
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
req.dll: Photometadatahandler.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Photometadatahandler.dll
api_name:
 - ITranscodeImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITranscodeImage interface


## -description


Exposes a method that allows conversion to JPEG or bitmap (BMP) image formats from any image type supported by Windows.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITranscodeImage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITranscodeImage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITranscodeImage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imagetranscode/nf-imagetranscode-itranscodeimage-transcodeimage">TranscodeImage</a>
</td>
<td align="left" width="63%">
Converts an image to JPEG or BMP image format.

</td>
</tr>
</table> 

