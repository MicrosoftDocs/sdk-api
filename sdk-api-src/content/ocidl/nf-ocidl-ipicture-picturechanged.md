---
UID: NF:ocidl.IPicture.PictureChanged
title: IPicture::PictureChanged
author: windows-sdk-content
description: Notifies the picture object that its picture resource has changed. This method only calls IPropertyNotifySink::OnChanged with DISPID_PICT_HANDLE for any connected sinks.
old-location: com\ipicture_picturechanged.htm
old-project: com
ms.assetid: 60485293-8d5b-4f9f-a529-746ea3371491
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPicture interface [COM],PictureChanged method, IPicture.PictureChanged, IPicture::PictureChanged, PictureChanged, PictureChanged method [COM], PictureChanged method [COM],IPicture interface, _ctrl_ipicture_picturechanged, com.ipicture_picturechanged, ocidl/IPicture::PictureChanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.PictureChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPicture::PictureChanged


## -description


Notifies the picture object that its picture resource has changed. This method only calls <a href="https://msdn.microsoft.com/71ab5206-5127-45f1-a2b5-3fbcc867d678">IPropertyNotifySink::OnChanged</a> with DISPID_PICT_HANDLE for any connected sinks.


## -parameters






## -returns



This method S_OK if it succeeds and E_FAIL if the picture object is uninitialized.




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>
 

 

