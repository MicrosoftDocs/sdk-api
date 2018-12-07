---
UID: NN:strmif.ICreateDevEnum
title: ICreateDevEnum
author: windows-sdk-content
description: The ICreateDevEnum interface creates an enumerator for a category of filters, such as video capture devices or audio capture devices.
old-location: dshow\icreatedevenum.htm
tech.root: DirectShow
ms.assetid: fc300bb8-aea4-4848-af43-a70a7fb8c07c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICreateDevEnum, ICreateDevEnum interface [DirectShow], ICreateDevEnum interface [DirectShow],described, ICreateDevEnumInterface, dshow.icreatedevenum, strmif/ICreateDevEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICreateDevEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateDevEnum interface


## -description


The <b>ICreateDevEnum</b> interface creates an enumerator for a category of filters, such as video capture devices or audio capture devices. The <a href="https://msdn.microsoft.com/ea98be7f-580d-4986-bd6b-d254a2c075e8">System Device Enumerator</a> exposes this interface.

Applications can use this interface to enumerate filters within a category. The <a href="https://msdn.microsoft.com/07457acc-51f1-4d1b-b795-e8d980a5531e">CreateClassEnumerator</a> method returns an enumerator object for a specific filter category. The enumerator object supports the <a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a> interface and returns a list of monikers, where each moniker represents a filter.

In some cases, the same DirectShow filter manages an entire category of hardware devices. In that case, the moniker represents the device, and the moniker is used to initialize the filter. The application can treat each device as a separate filter, regardless of the underlying implementation.

For more information on using this interface, see <a href="https://msdn.microsoft.com/70db139c-2c5b-4574-bec3-dfe758b16715">Using the System Device Enumerator</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateDevEnum</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateDevEnum</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateDevEnum</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07457acc-51f1-4d1b-b795-e8d980a5531e">CreateClassEnumerator</a>
</td>
<td align="left" width="63%">
Creates a class enumerator for a specified device category.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>



<a href="https://msdn.microsoft.com/70db139c-2c5b-4574-bec3-dfe758b16715">Using the System Device Enumerator</a>
 

 

