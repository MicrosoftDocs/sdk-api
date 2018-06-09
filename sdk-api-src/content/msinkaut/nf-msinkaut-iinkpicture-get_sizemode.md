---
UID: NF:msinkaut.IInkPicture.get_SizeMode
title: IInkPicture::get_SizeMode
author: windows-sdk-content
description: Gets or sets how the InkPicture control handles image placement and sizing.
old-location: tablet\inkpicture_sizemode.htm
old-project: tablet
ms.assetid: 3ce10b92-80d4-4517-92cb-eff10fc8c0ba
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IInkPicture interface [Tablet PC],SizeMode property, IInkPicture.SizeMode, IInkPicture.get_SizeMode, IInkPicture::SizeMode, IInkPicture::get_SizeMode, IInkPicture::put_SizeMode, InkPicture.get_SizeMode, InkPicture.put_SizeMode, SizeMode property [Tablet PC], SizeMode property [Tablet PC],IInkPicture interface, get_SizeMode, msinkaut/IInkPicture::SizeMode, msinkaut/IInkPicture::get_SizeMode, msinkaut/IInkPicture::put_SizeMode, put_SizeMode, tablet.inkpicture_sizemode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::get_SizeMode


## -description


Gets or sets how the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control handles image placement and sizing.


This property is read/write.


## -parameters


## -remarks



Valid values for this property are taken from the <a href="https://msdn.microsoft.com/e24c38b4-b25f-4d0e-88f5-f56f5dc6be1a">InkPictureSizeMode</a> enumeration. By default, in <b>IPSM_Normal</b> mode, the picture is positioned in the upper-left corner of the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control, and any part of the image too big for the InkPicture control is clipped. Using the <b>IPSM_StretchImage</b> value causes the picture to stretch to fit the control.



Using the <b>IPSM_AutoSize</b> value causes the control to resize to always fit the picture. Using the <b>IPSM_CenterImage</b> value causes the picture to be centered in the control.






## -see-also




<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/e24c38b4-b25f-4d0e-88f5-f56f5dc6be1a">InkPictureSizeMode</a>
 

 

