---
UID: NF:control.IMediaControl.get_FilterCollection
title: IMediaControl::get_FilterCollection
author: windows-sdk-content
description: The get_FilterCollection method retrieves a collection of the filters in the filter graph.
old-location: dshow\imediacontrol_get_filtercollection.htm
old-project: DirectShow
ms.assetid: 9a14e971-365e-4061-8d07-01216e793864
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMediaControl interface [DirectShow],get_FilterCollection method, IMediaControl.get_FilterCollection, IMediaControl::get_FilterCollection, IMediaControlget_FilterCollection, control/IMediaControl::get_FilterCollection, dshow.imediacontrol_get_filtercollection, get_FilterCollection, get_FilterCollection method [DirectShow], get_FilterCollection method [DirectShow],IMediaControl interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
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
tech.root: 
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaControl.get_FilterCollection
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaControl::get_FilterCollection


## -description



The <code>get_FilterCollection</code> method retrieves a collection of the filters in the filter graph.



This method is intended for use by Visual Basic 6.0 applications. It was documented for Visual Basic 6.0 as the <b>FilgraphManager.FilterCollection</b> property. C++ applications should use the <a href="https://msdn.microsoft.com/3a6dcd1a-3ec3-4f0f-8e82-2d33ad775eec">IFilterGraph::EnumFilters</a> method instead.


## -parameters




### -param ppUnk [out]

Receives a pointer to the <b>IDispatch</b> interface.  The caller must release the interface. You can query the returned pointer for the <b>IAMCollection</b> interface. The collection contains a list of <b>IFilterInfo</b> pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl Interface</a>
 

 

