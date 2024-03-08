---
UID: NF:d2d1_1.ID2D1Device.CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,constD2D1_PRINT_CONTROL_PROPERTIES&,ID2D1PrintControl)
title: ID2D1Device::CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES &,ID2D1PrintControl) (d2d1_1.h)
description: Creates an ID2D1PrintControl object that converts Direct2D primitives stored in ID2D1CommandList into a fixed page representation. The print sub-system then consumes the primitives. (overload 2/2)
helpviewer_keywords: ["CreatePrintControl","CreatePrintControl method [Direct2D]","CreatePrintControl method [Direct2D]","ID2D1Device interface","ID2D1Device interface [Direct2D]","CreatePrintControl method","ID2D1Device.CreatePrintControl","ID2D1Device.CreatePrintControl(IWICImagingFactory","IPrintDocumentPackageTarget","const D2D1_PRINT_CONTROL_PROPERTIES &","ID2D1PrintControl)","ID2D1Device::CreatePrintControl","ID2D1Device::CreatePrintControl(IWICImagingFactory","IPrintDocumentPackageTarget","const D2D1_PRINT_CONTROL_PROPERTIES &","ID2D1PrintControl)","d2d1_1/ID2D1Device::CreatePrintControl","direct2d.id2d1device_createprintcontrol2"]
old-location: direct2d\id2d1device_createprintcontrol2.htm
tech.root: Direct2D
ms.assetid: 7F1BE691-2CC4-4A53-9D4D-42E3D7354509
ms.date: 12/05/2018
ms.keywords: CreatePrintControl, CreatePrintControl method [Direct2D], CreatePrintControl method [Direct2D],ID2D1Device interface, ID2D1Device interface [Direct2D],CreatePrintControl method, ID2D1Device.CreatePrintControl, ID2D1Device.CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES &,ID2D1PrintControl), ID2D1Device::CreatePrintControl, ID2D1Device::CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES &,ID2D1PrintControl), d2d1_1/ID2D1Device::CreatePrintControl, direct2d.id2d1device_createprintcontrol2
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Device::CreatePrintControl
 - d2d1_1/ID2D1Device::CreatePrintControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device.CreatePrintControl
---

# ID2D1Device::CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES &,ID2D1PrintControl)


## -description

Creates an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a> object that converts <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> primitives stored in <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> into a fixed page representation.  The print sub-system then consumes the primitives.

## -parameters

### -param wicFactory [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>*</b>

A WIC imaging factory.

### -param documentTarget [in]

Type: <b><a href="/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget">IPrintDocumentPackageTarget</a>*</b>

The target print job for this control.

### -param printControlProperties [in, ref, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_print_control_properties">D2D1_PRINT_CONTROL_PROPERTIES</a></b>

The options to be applied to the print control.

### -param printControl [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a>**</b>

When this method returns, contains the address of a pointer to an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a> object.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>Generic failure code.</td>
</tr>
<tr>
<td>D2DERR_PRINT_FORMAT_NOT_SUPPORTED</td>
<td>The print format is not supported by the document target.</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.
</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>
