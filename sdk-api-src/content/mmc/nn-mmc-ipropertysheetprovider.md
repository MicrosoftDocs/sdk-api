---
UID: NN:mmc.IPropertySheetProvider
title: IPropertySheetProvider (mmc.h)
description: The IPropertySheetProvider interface implements Windows property sheets as COM objects.
helpviewer_keywords: ["IPropertySheetProvider","IPropertySheetProvider interface [MMC]","IPropertySheetProvider interface [MMC]","described","_slate_ipropertysheetprovider","mmc.ipropertysheetprovider","mmc/IPropertySheetProvider"]
old-location: mmc\ipropertysheetprovider.htm
tech.root: mmc
ms.assetid: c63d5d5f-a334-4367-8a1e-252b4eb5b50d
ms.date: 12/05/2018
ms.keywords: IPropertySheetProvider, IPropertySheetProvider interface [MMC], IPropertySheetProvider interface [MMC],described, _slate_ipropertysheetprovider, mmc.ipropertysheetprovider, mmc/IPropertySheetProvider
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertySheetProvider
 - mmc/IPropertySheetProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider
---

# IPropertySheetProvider interface


## -description

The 
<b>IPropertySheetProvider</b> interface implements Windows property sheets as COM objects. A property sheet object contains the code required to handle modeless operation and determining which other snap-ins are extending the node type. The size of the property sheet is set by the primary snap-in and extensions are forced to accept that size.

## -inheritance

The <b>IPropertySheetProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertySheetProvider</b> also has these types of members:

