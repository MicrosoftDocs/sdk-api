---
UID: NF:faxcom.IFaxTiff.get_TiffTagString
title: IFaxTiff::get_TiffTagString
author: windows-sdk-content
description: Retrieves the TiffTagString property for a FaxTiff object. The TiffTagString property is a null-terminated string that contains the value of a specified Tagged Image File Format (TIFF) tag (field).
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_tifftagstring_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1pif.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxTiff interface [Fax Service],TiffTagString property, IFaxTiff.TiffTagString, IFaxTiff.get_TiffTagString, IFaxTiff::TiffTagString, IFaxTiff::get_TiffTagString, IFaxTiff::put_TiffTagString, TiffTagString property [Fax Service], TiffTagString property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_tifftagstring, fax._mfax_ifaxtiff_get_tifftagstring, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_tifftagstring_cpp, faxcom/IFaxTiff::TiffTagString, faxcom/IFaxTiff::get_TiffTagString, faxcom/IFaxTiff::put_TiffTagString, get_TiffTagString
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
req.lib: 
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxTiff.TiffTagString
 - IFaxTiff.get_TiffTagString
 - IFaxTiff.put_TiffTagString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxTiff::get_TiffTagString


## -description


Retrieves the <b>TiffTagString</b> property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object. The <b>TiffTagString</b> property is a null-terminated string that contains the value of a specified Tagged Image File Format (TIFF) tag (field).

This property is read/write.


## -parameters


## -remarks



For more information about Tagged Image File Format Class F (TIFF Class F) files, see <a href="https://msdn.microsoft.com/d7840c10-6059-40ed-9040-50eefefc7349">Fax Image Format</a>. For current information about TIFF tags, or for the list of valid TIFF tag numbers, contact Adobe Systems Incorporated.

A fax client application must  set the <a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object.

The <b>get_TiffTagString</b> method sets the <i>pVal</i> parameter to a string that represents the value of the TIFF tag, if it is available. If the information is not available, the method returns "Unavailable".

The <b>TiffTagString</b> property is a string that represents the value of the TIFF tag, if it is available. If the information is not available, <b>TiffTagString</b> is an empty string.

You can call the <b>get_TiffTagString</b> to retrieve information about any TIFF tag, including those that the fax service does not support. Note that you can retrieve this property only for the first page of a TIFF file.

The <b>TiffTagString</b> property contains information about any TIFF tag, including those that the fax service does not support. Note that this property only contains information for the first page of a TIFF file.

The <b>get_TiffTagString</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/a4c46893-502d-4d5c-a895-837cffc014e4">IFaxTiff</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

