---
UID: NF:wiavideo.IWiaVideo.put_ImagesDirectory
title: IWiaVideo::put_ImagesDirectory (wiavideo.h)
description: The IWiaVideo::ImagesDirectory property specifies the full path and directory where images are stored when calling the IWiaVideo::TakePicture method.
helpviewer_keywords: ["IWiaVideo interface [WIA]","ImagesDirectory property","IWiaVideo.ImagesDirectory","IWiaVideo.put_ImagesDirectory","IWiaVideo::ImagesDirectory","IWiaVideo::get_ImagesDirectory","IWiaVideo::put_ImagesDirectory","ImagesDirectory property [WIA]","ImagesDirectory property [WIA]","IWiaVideo interface","_wia_IWiaVideo_ImagesDirectory","put_ImagesDirectory","wia._wia_IWiaVideo_ImagesDirectory","wiavideo/IWiaVideo::ImagesDirectory","wiavideo/IWiaVideo::get_ImagesDirectory","wiavideo/IWiaVideo::put_ImagesDirectory"]
old-location: wia\_wia_IWiaVideo_ImagesDirectory.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\imagesdirectory.htm
ms.date: 12/05/2018
ms.keywords: IWiaVideo interface [WIA],ImagesDirectory property, IWiaVideo.ImagesDirectory, IWiaVideo.put_ImagesDirectory, IWiaVideo::ImagesDirectory, IWiaVideo::get_ImagesDirectory, IWiaVideo::put_ImagesDirectory, ImagesDirectory property [WIA], ImagesDirectory property [WIA],IWiaVideo interface, _wia_IWiaVideo_ImagesDirectory, put_ImagesDirectory, wia._wia_IWiaVideo_ImagesDirectory, wiavideo/IWiaVideo::ImagesDirectory, wiavideo/IWiaVideo::get_ImagesDirectory, wiavideo/IWiaVideo::put_ImagesDirectory
f1_keywords:
- wiavideo/IWiaVideo.ImagesDirectory
dev_langs:
- c++
req.header: wiavideo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Wiavideo.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wiavideo.dll
api_name:
- IWiaVideo.ImagesDirectory
- IWiaVideo.get_ImagesDirectory
- IWiaVideo.put_ImagesDirectory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWiaVideo::put_ImagesDirectory


## -description


The <b>IWiaVideo::ImagesDirectory</b> property specifies the full path and directory where images are stored when calling the <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-takepicture">IWiaVideo::TakePicture</a> method.

This property is read/write.


## -parameters


## -remarks



This property should be set to the value of the video device's WIA_DPV_IMAGES_DIRECTORY property.



