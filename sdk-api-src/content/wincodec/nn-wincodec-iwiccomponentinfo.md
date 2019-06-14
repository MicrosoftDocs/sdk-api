---
UID: NN:wincodec.IWICComponentInfo
title: IWICComponentInfo (wincodec.h)
author: windows-sdk-content
description: Exposes methods that provide component information.
old-location: wic\_wic_codec_iwiccomponentinfo.htm
tech.root: wic
ms.assetid: a31267ed-60cd-4de9-9fed-26bb390b29e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICComponentInfo, IWICComponentInfo interface [Windows Imaging Component], IWICComponentInfo interface [Windows Imaging Component],described, _wic_codec_iwiccomponentinfo, wic._wic_codec_iwiccomponentinfo, wincodec/IWICComponentInfo
ms.topic: interface
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICComponentInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICComponentInfo interface


## -description


Exposes methods that provide component information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICComponentInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICComponentInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICComponentInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getauthor">GetAuthor</a>
</td>
<td align="left" width="63%">
Retrieves the name of component's author.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getclsid">GetCLSID</a>
</td>
<td align="left" width="63%">
Retrieves the component's CLSID

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getcomponenttype">GetComponentType</a>
</td>
<td align="left" width="63%">
Retrieves the component's <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccomponenttype">WICComponentType</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the component's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getsigningstatus">GetSigningStatus</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccomponentsigning">WICComponentSigning</a> status of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getspecversion">GetSpecVersion</a>
</td>
<td align="left" width="63%">
Retrieves the component's specification version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getvendorguid">GetVendorGUID</a>
</td>
<td align="left" width="63%">
Retrieves the vendor GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwiccomponentinfo-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the component's version. 

</td>
</tr>
</table> 

