---
UID: NN:mmc.IPropertySheetProvider
title: IPropertySheetProvider (mmc.h)

description: The IPropertySheetProvider interface implements Windows property sheets as COM objects.
old-location: mmc\ipropertysheetprovider.htm
tech.root: mmc
ms.assetid: c63d5d5f-a334-4367-8a1e-252b4eb5b50d

ms.date: 12/05/2018
ms.keywords: IPropertySheetProvider, IPropertySheetProvider interface [MMC], IPropertySheetProvider interface [MMC],described, _slate_ipropertysheetprovider, mmc.ipropertysheetprovider, mmc/IPropertySheetProvider
ms.topic: interface
f1_keywords: 
 - "mmc/IPropertySheetProvider"
dev_langs:
 - c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertySheetProvider interface


## -description


The 
<b>IPropertySheetProvider</b> interface implements Windows property sheets as COM objects. A property sheet object contains the code required to handle modeless operation and determining which other snap-ins are extending the node type. The size of the property sheet is set by the primary snap-in and extensions are forced to accept that size.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertySheetProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertySheetProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertySheetProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addextensionpages">AddExtensionPages</a>
</td>
<td align="left" width="63%">
Collects pages from one or more extension snap-ins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addprimarypages">AddPrimaryPages</a>
</td>
<td align="left" width="63%">
Collects property pages from the primary snap-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-createpropertysheet">CreatePropertySheet</a>
</td>
<td align="left" width="63%">
Creates a property sheet frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-findpropertysheet">FindPropertySheet</a>
</td>
<td align="left" width="63%">
Determines whether a property sheet exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-show">Show</a>
</td>
<td align="left" width="63%">
Displays a specific property sheet frame.

</td>
</tr>
</table> 

