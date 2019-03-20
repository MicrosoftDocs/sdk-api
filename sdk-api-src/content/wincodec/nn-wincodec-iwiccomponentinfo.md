---
UID: NN:wincodec.IWICComponentInfo
title: IWICComponentInfo (wincodec.h)
author: windows-sdk-content
description: Exposes methods that provide component information.
old-location: wic\_wic_codec_iwiccomponentinfo.htm
tech.root: wic
ms.assetid: a31267ed-60cd-4de9-9fed-26bb390b29e6
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# IWICComponentInfo interface


## -description


Exposes methods that provide component information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICComponentInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICComponentInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c92f707f-6077-4da0-9ac4-6d1f30fb5b75">GetAuthor</a>
</td>
<td align="left" width="63%">
Retrieves the name of component's author.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63814933-1366-47b9-8cf4-0d8685053a30">GetCLSID</a>
</td>
<td align="left" width="63%">
Retrieves the component's CLSID

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7599299-2854-4796-8760-740a6ae7ad4f">GetComponentType</a>
</td>
<td align="left" width="63%">
Retrieves the component's <a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c67e7a30-8bd5-427b-8a67-c77e3cf86e78">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the component's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6d13240-3750-4450-8069-7e05dd89f2ab">GetSigningStatus</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/64f3de6d-15da-4cc8-ad74-57759bcd4d07">WICComponentSigning</a> status of the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18a771c7-8764-4694-be05-29c5eda27e93">GetSpecVersion</a>
</td>
<td align="left" width="63%">
Retrieves the component's specification version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1ef7bac-6845-4e7f-8cb6-bb3270b344d6">GetVendorGUID</a>
</td>
<td align="left" width="63%">
Retrieves the vendor GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f65d13ae-ccec-49a8-8818-225464b3a117">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the component's version. 

</td>
</tr>
</table> 

