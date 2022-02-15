---
UID: NF:ocidl.IPicture.PictureChanged
title: IPicture::PictureChanged (ocidl.h)
description: Notifies the picture object that its picture resource has changed. This method only calls IPropertyNotifySink::OnChanged with DISPID_PICT_HANDLE for any connected sinks.
helpviewer_keywords: ["IPicture interface [COM]","PictureChanged method","IPicture.PictureChanged","IPicture::PictureChanged","PictureChanged","PictureChanged method [COM]","PictureChanged method [COM]","IPicture interface","_ctrl_ipicture_picturechanged","com.ipicture_picturechanged","ocidl/IPicture::PictureChanged"]
old-location: com\ipicture_picturechanged.htm
tech.root: com
ms.assetid: 60485293-8d5b-4f9f-a529-746ea3371491
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],PictureChanged method, IPicture.PictureChanged, IPicture::PictureChanged, PictureChanged, PictureChanged method [COM], PictureChanged method [COM],IPicture interface, _ctrl_ipicture_picturechanged, com.ipicture_picturechanged, ocidl/IPicture::PictureChanged
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPicture::PictureChanged
 - ocidl/IPicture::PictureChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.PictureChanged
---

# IPicture::PictureChanged


## -description

Notifies the picture object that its picture resource has changed. This method only calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertynotifysink-onchanged">IPropertyNotifySink::OnChanged</a> with DISPID_PICT_HANDLE for any connected sinks.



## -returns

This method S_OK if it succeeds and E_FAIL if the picture object is uninitialized.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>
