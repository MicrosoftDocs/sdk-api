---
UID: NF:msinkaut.IInkPicture.get_SizeMode
title: IInkPicture::get_SizeMode (msinkaut.h)
description: Gets or sets how the InkPicture control handles image placement and sizing.helpviewer_keywords: ["IInkPicture interface [Tablet PC]","SizeMode property","IInkPicture.SizeMode","IInkPicture.get_SizeMode","IInkPicture::SizeMode","IInkPicture::get_SizeMode","IInkPicture::put_SizeMode","InkPicture.get_SizeMode","InkPicture.put_SizeMode","SizeMode property [Tablet PC]","SizeMode property [Tablet PC]","IInkPicture interface","get_SizeMode","msinkaut/IInkPicture::SizeMode","msinkaut/IInkPicture::get_SizeMode","msinkaut/IInkPicture::put_SizeMode","put_SizeMode","tablet.inkpicture_sizemode"]
old-location: tablet\inkpicture_sizemode.htm
tech.root: tablet
ms.assetid: 3ce10b92-80d4-4517-92cb-eff10fc8c0ba
ms.date: 12/05/2018
ms.keywords: IInkPicture interface [Tablet PC],SizeMode property, IInkPicture.SizeMode, IInkPicture.get_SizeMode, IInkPicture::SizeMode, IInkPicture::get_SizeMode, IInkPicture::put_SizeMode, InkPicture.get_SizeMode, InkPicture.put_SizeMode, SizeMode property [Tablet PC], SizeMode property [Tablet PC],IInkPicture interface, get_SizeMode, msinkaut/IInkPicture::SizeMode, msinkaut/IInkPicture::get_SizeMode, msinkaut/IInkPicture::put_SizeMode, put_SizeMode, tablet.inkpicture_sizemode
f1_keywords:
- msinkaut/IInkPicture.SizeMode
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkPicture.SizeMode
- IInkPicture.get_SizeMode
- IInkPicture.put_SizeMode
- InkPicture.get_SizeMode
- InkPicture.put_SizeMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkPicture::get_SizeMode


## -description


Gets or sets how the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control handles image placement and sizing.


This property is read/write.


## -parameters


## -remarks



Valid values for this property are taken from the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode">InkPictureSizeMode</a> enumeration. By default, in <b>IPSM_Normal</b> mode, the picture is positioned in the upper-left corner of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control, and any part of the image too big for the InkPicture control is clipped. Using the <b>IPSM_StretchImage</b> value causes the picture to stretch to fit the control.



Using the <b>IPSM_AutoSize</b> value causes the control to resize to always fit the picture. Using the <b>IPSM_CenterImage</b> value causes the picture to be centered in the control.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode">InkPictureSizeMode</a>
 

 

