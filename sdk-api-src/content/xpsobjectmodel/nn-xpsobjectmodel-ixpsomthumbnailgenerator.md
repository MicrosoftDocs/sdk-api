---
UID: NN:xpsobjectmodel.IXpsOMThumbnailGenerator
title: IXpsOMThumbnailGenerator (xpsobjectmodel.h)
description: Generates a thumbnail image resource.
helpviewer_keywords: ["IXpsOMThumbnailGenerator","IXpsOMThumbnailGenerator interface [XPS Documents and Packaging]","IXpsOMThumbnailGenerator interface [XPS Documents and Packaging]","described","xps.ixpsomthumbnailgenerator","xpsobjectmodel/IXpsOMThumbnailGenerator"]
old-location: xps\ixpsomthumbnailgenerator.htm
tech.root: xps
ms.assetid: cac794c0-bea2-417e-880f-15838f718ba7
ms.date: 12/05/2018
ms.keywords: IXpsOMThumbnailGenerator, IXpsOMThumbnailGenerator interface [XPS Documents and Packaging], IXpsOMThumbnailGenerator interface [XPS Documents and Packaging],described, xps.ixpsomthumbnailgenerator, xpsobjectmodel/IXpsOMThumbnailGenerator
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: XpsRasterService.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMThumbnailGenerator
 - xpsobjectmodel/IXpsOMThumbnailGenerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsRasterService.dll
api_name:
 - IXpsOMThumbnailGenerator
---

# IXpsOMThumbnailGenerator interface


## -description

Generates a thumbnail image resource.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMThumbnailGenerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMThumbnailGenerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMThumbnailGenerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomthumbnailgenerator-generatethumbnail">GenerateThumbnail</a>
</td>
<td align="left" width="63%">
Generates a thumbnail image of a page.

</td>
</tr>
</table>

## -remarks

To instantiate this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> as shown in the code example that follows.


```cpp

IXpsOMThumbnailGenerator    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
      __uuidof(XpsOMThumbnailGenerator),
      NULL, 
      CLSCTX_INPROC_SERVER,
      __uuidof(IXpsOMThumbnailGenerator),
      reinterpret_cast<LPVOID*>(&newInterface)
      );

if (SUCCEEDED(hr))
{
    // use newInterface
    newInterface->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
 

```


This interface requires XpsRasterService.dll. 
If XpsRasterService.dll is not present when <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> is called to create an <b>IXpsOMThumbnailGenerator</b> instance, <b>CoCreateInstance</b> returns E_FAIL.

## -see-also

<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>