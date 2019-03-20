---
UID: NF:faxcom.IFaxTiff.get_TiffTagString
title: IFaxTiff::get_TiffTagString (faxcom.h)
author: windows-sdk-content
description: Retrieves the TiffTagString property for a FaxTiff object. The TiffTagString property is a null-terminated string that contains the value of a specified Tagged Image File Format (TIFF) tag (field).
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_tifftagstring_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1pif.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxTiff interface [Fax Service],TiffTagString property, IFaxTiff.TiffTagString, IFaxTiff.get_TiffTagString, IFaxTiff::TiffTagString, IFaxTiff::get_TiffTagString, IFaxTiff::put_TiffTagString, TiffTagString property [Fax Service], TiffTagString property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_tifftagstring, fax._mfax_ifaxtiff_get_tifftagstring, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_tifftagstring_cpp, faxcom/IFaxTiff::TiffTagString, faxcom/IFaxTiff::get_TiffTagString, faxcom/IFaxTiff::put_TiffTagString, get_TiffTagString
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


Retrieves the <b>TiffTagString</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object. The <b>TiffTagString</b> property is a null-terminated string that contains the value of a specified Tagged Image File Format (TIFF) tag (field).

This property is read/write.


## -parameters


## -remarks



For more information about Tagged Image File Format Class F (TIFF Class F) files, see <a href="https://msdn.microsoft.com/en-us/library/ms693440(v=VS.85).aspx">Fax Image Format</a>. For current information about TIFF tags, or for the list of valid TIFF tag numbers, contact Adobe Systems Incorporated.

A fax client application must  set the <a href="https://msdn.microsoft.com/en-us/library/ms690773(v=VS.85).aspx">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object.

The <b>get_TiffTagString</b> method sets the <i>pVal</i> parameter to a string that represents the value of the TIFF tag, if it is available. If the information is not available, the method returns "Unavailable".

The <b>TiffTagString</b> property is a string that represents the value of the TIFF tag, if it is available. If the information is not available, <b>TiffTagString</b> is an empty string.

You can call the <b>get_TiffTagString</b> to retrieve information about any TIFF tag, including those that the fax service does not support. Note that you can retrieve this property only for the first page of a TIFF file.

The <b>TiffTagString</b> property contains information about any TIFF tag, including those that the fax service does not support. Note that this property only contains information for the first page of a TIFF file.

The <b>get_TiffTagString</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691802(v=VS.85).aspx">IFaxTiff</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

