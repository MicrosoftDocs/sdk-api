---
UID: NF:faxcom.IFaxTiff.get_Image
title: IFaxTiff::get_Image method
author: windows-driver-content
description: Sets or retrieves the Image property for a FaxTiff object.
old-location: fax\_mfax_ifaxtiff_get_image_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0cdh.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: FaxTiff object [Fax Service], Image property, IFaxTiff, IFaxTiff::get_Image, Image property [Fax Service], Image property [Fax Service], FaxTiff object, _mfax_ifaxtiff_get_image, fax._mfax_ifaxtiff_get_image, fax._mfax_ifaxtiff_get_image_vb, get_Image,IFaxTiff.get_Image
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxTiff.Image
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxTiff::get_Image method


## -description


Sets or retrieves the <b>Image</b> property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object. The <b>Image</b> property is a null-terminated string that contains the full path and file name of the file represented by the FaxTiff object. The file is a Tagged Image File Format Class F (TIFF Class F) file.

This property is read/write.


## -parameters


## -remarks



A fax client application must  set the <b>Image</b> property before retrieving another property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object.

A fax client application can call the <b>get_Image</b> retrieval method to determine the name of the facsimile image file that is open as a result of a successful call to the <b>put_Image</b> method.

A fax client application can use this retrieval method to determine the name of the facsimile image file that is open as a result of successful assignment of the <b>Image</b> property.

The <b>get_Image</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/98d385be-cebb-428e-92f7-22a1fc814c3c">FaxTiff</a>



<a href="https://msdn.microsoft.com/a4c46893-502d-4d5c-a895-837cffc014e4">IFaxTiff</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

