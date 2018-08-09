---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromSource
title: IWICImagingFactory::CreateBitmapFromSource
author: windows-sdk-content
description: Creates a IWICBitmap from a IWICBitmapSource.
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfromsource.htm
old-project: wic
ms.assetid: b3b9057f-e39a-4e7b-a3dc-0942d55c25e0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateBitmapFromSource, CreateBitmapFromSource method [Windows Imaging Component], CreateBitmapFromSource method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromSource method, IWICImagingFactory.CreateBitmapFromSource, IWICImagingFactory::CreateBitmapFromSource, WICBitmapCacheOnDemand, WICBitmapCacheOnLoad, WICBitmapNoCache, _wic_codec_iwicimagingfactory_createbitmapfromsource, wic._wic_codec_iwicimagingfactory_createbitmapfromsource, wincodec/IWICImagingFactory::CreateBitmapFromSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICImagingFactory.CreateBitmapFromSource
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateBitmapFromSource


## -description


Creates a <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from a <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>.


## -parameters




### -param pIBitmapSource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> to create the bitmap from.


### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/121d394d-e818-44c5-bf44-3b01df61c780">WICBitmapCreateCacheOption</a></b>

The cache options of the new bitmap.  This can be one of the values in the <a href="https://msdn.microsoft.com/121d394d-e818-44c5-bf44-3b01df61c780">WICBitmapCreateCacheOption</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WICBitmapNoCache"></a><a id="wicbitmapnocache"></a><a id="WICBITMAPNOCACHE"></a><dl>
<dt><b>WICBitmapNoCache</b></dt>
</dl>
</td>
<td width="60%">
Do not create a system memory copy. Share the bitmap with the source.


</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnDemand"></a><a id="wicbitmapcacheondemand"></a><a id="WICBITMAPCACHEONDEMAND"></a><dl>
<dt><b>WICBitmapCacheOnDemand</b></dt>
</dl>
</td>
<td width="60%">
Create a system memory copy when the bitmap is first used.


</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnLoad"></a><a id="wicbitmapcacheonload"></a><a id="WICBITMAPCACHEONLOAD"></a><dl>
<dt><b>WICBitmapCacheOnLoad</b></dt>
</dl>
</td>
<td width="60%">
Create a system memory copy when this method is called.


</td>
</tr>
</table>
 


### -param ppIBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



