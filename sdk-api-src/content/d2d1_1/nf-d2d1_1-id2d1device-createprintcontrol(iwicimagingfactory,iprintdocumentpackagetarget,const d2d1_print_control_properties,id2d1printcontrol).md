---
UID: NF:d2d1_1.ID2D1Device.CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES,ID2D1PrintControl)
title: ID2D1Device::CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES,ID2D1PrintControl)
author: windows-sdk-content
description: Creates an ID2D1PrintControl object that converts Direct2D primitives stored in ID2D1CommandList into a fixed page representation. The print sub-system then consumes the primitives.
old-location: direct2d\id2d1device_createxpsprintcontrol.htm
tech.root: direct2d
ms.assetid: dcffa436-154a-4283-9c1c-f167de5f9888
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreatePrintControl, CreatePrintControl method [Direct2D], CreatePrintControl method [Direct2D],ID2D1Device interface, ID2D1Device interface [Direct2D],CreatePrintControl method, ID2D1Device.CreatePrintControl, ID2D1Device.CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES,ID2D1PrintControl), ID2D1Device::CreatePrintControl, ID2D1Device::CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES,ID2D1PrintControl), d2d1_1/ID2D1Device::CreatePrintControl, direct2d.id2d1device_createxpsprintcontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device.CreatePrintControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device::CreatePrintControl(IWICImagingFactory,IPrintDocumentPackageTarget,const D2D1_PRINT_CONTROL_PROPERTIES,ID2D1PrintControl)


## -description


Creates an <a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a> object that converts <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> primitives stored in <a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a> into a fixed page representation.  The print sub-system then consumes the primitives.


## -parameters




### -param wicFactory [in]

Type: <b><a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>*</b>

A WIC imaging factory.


### -param documentTarget [in]

Type: <b><a href="https://msdn.microsoft.com/0F63C626-DB58-4952-BBB3-7E3901429C35">IPrintDocumentPackageTarget</a>*</b>

The target print job for this control.


### -param printControlProperties [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/5A4D4DDC-4161-44A2-9EB6-E4C14696B810">D2D1_PRINT_CONTROL_PROPERTIES</a>*</b>

The options to be applied to the print control.


### -param printControl [out]

Type: <b><a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a>**</b>

When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a> object.


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




<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>
 

 

