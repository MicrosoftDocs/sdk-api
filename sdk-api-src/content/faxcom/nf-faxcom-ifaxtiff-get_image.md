---
UID: NF:faxcom.IFaxTiff.get_Image
title: IFaxTiff::get_Image (faxcom.h)
description: Sets or retrieves the Image property for a FaxTiff object. (Get)
helpviewer_keywords: ["IFaxTiff interface [Fax Service]","Image property","IFaxTiff.Image","IFaxTiff.get_Image","IFaxTiff::Image","IFaxTiff::get_Image","IFaxTiff::put_Image","Image property [Fax Service]","Image property [Fax Service]","IFaxTiff interface","_mfax_ifaxtiff_get_image","fax._mfax_ifaxtiff_get_image","fax._mfax_ifaxtiff_mfax_ifaxtiff_get_image_cpp","faxcom/IFaxTiff::Image","faxcom/IFaxTiff::get_Image","faxcom/IFaxTiff::put_Image","get_Image"]
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_image_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0cdh.htm
ms.date: 12/05/2018
ms.keywords: IFaxTiff interface [Fax Service],Image property, IFaxTiff.Image, IFaxTiff.get_Image, IFaxTiff::Image, IFaxTiff::get_Image, IFaxTiff::put_Image, Image property [Fax Service], Image property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_image, fax._mfax_ifaxtiff_get_image, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_image_cpp, faxcom/IFaxTiff::Image, faxcom/IFaxTiff::get_Image, faxcom/IFaxTiff::put_Image, get_Image
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
req.lib: 
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxTiff::get_Image
 - faxcom/IFaxTiff::get_Image
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxTiff.Image
 - IFaxTiff.get_Image
 - IFaxTiff.put_Image
---

# IFaxTiff::get_Image


## -description

Sets or retrieves the <b>Image</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. The <b>Image</b> property is a null-terminated string that contains the full path and file name of the file represented by the FaxTiff object. The file is a Tagged Image File Format Class F (TIFF Class F) file.

This property is read/write.

## -parameters

## -remarks

A fax client application must  set the <b>Image</b> property before retrieving another property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

A fax client application can call the <b>get_Image</b> retrieval method to determine the name of the facsimile image file that is open as a result of a successful call to the <b>put_Image</b> method.

A fax client application can use this retrieval method to determine the name of the facsimile image file that is open as a result of successful assignment of the <b>Image</b> property.

The <b>get_Image</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
