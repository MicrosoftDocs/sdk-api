---
UID: NF:ocidl.IPicture.set_hPal
title: IPicture::set_hPal
author: windows-driver-content
description: Assigns a GDI palette to the picture contained in the picture object.
old-location: com\ipicture_set_hpal.htm
old-project: com
ms.assetid: c20b9efd-cf85-4ee1-890b-35fde0226982
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IPicture interface [COM],set_hPal method, IPicture.set_hPal, IPicture::set_hPal, _ctrl_ipicture_set_hpal, com.ipicture_set_hpal, ocidl/IPicture::set_hPal, set_hPal, set_hPal method [COM], set_hPal method [COM],IPicture interface
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPicture.set_hPal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPicture::set_hPal


## -description


Assigns a GDI palette to the picture contained in the picture object.


## -parameters




### -param hPal [in]

A handle to the GDI palette assigned to the picture.


## -returns



This method supports the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Ownership of the palette passed to this method depends on how the picture object was created, as specified by the <i>fOwn</i> parameter to <a href="https://msdn.microsoft.com/fb021348-07d4-4974-a71e-abb1b8d760c4">OleCreatePictureIndirect</a>. <a href="https://msdn.microsoft.com/de1847cd-ecc0-4941-9dbc-a60b8ef0b1c1">OleLoadPicture</a> forces <i>fOwn</i> to <b>TRUE</b>; if the object owns the picture, then it takes over ownership of this palette.




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>
 

 

