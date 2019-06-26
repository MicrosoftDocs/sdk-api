---
UID: NF:control.IMediaControl.get_FilterCollection
title: IMediaControl::get_FilterCollection (control.h)
author: windows-sdk-content
description: The get_FilterCollection method retrieves a collection of the filters in the filter graph.
old-location: dshow\imediacontrol_get_filtercollection.htm
tech.root: DirectShow
ms.assetid: 9a14e971-365e-4061-8d07-01216e793864
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaControl interface [DirectShow],get_FilterCollection method, IMediaControl.get_FilterCollection, IMediaControl::get_FilterCollection, IMediaControlget_FilterCollection, control/IMediaControl::get_FilterCollection, dshow.imediacontrol_get_filtercollection, get_FilterCollection, get_FilterCollection method [DirectShow], get_FilterCollection method [DirectShow],IMediaControl interface
ms.topic: method
f1_keywords: 
 - "control/IMediaControl.get_FilterCollection"
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
 - IMediaControl.get_FilterCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaControl::get_FilterCollection


## -description



The <code>get_FilterCollection</code> method retrieves a collection of the filters in the filter graph.



This method is intended for use by Visual Basic 6.0 applications. It was documented for Visual Basic 6.0 as the <b>FilgraphManager.FilterCollection</b> property. C++ applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-enumfilters">IFilterGraph::EnumFilters</a> method instead.


## -parameters




### -param ppUnk [out]

Receives a pointer to the <b>IDispatch</b> interface.  The caller must release the interface. You can query the returned pointer for the <b>IAMCollection</b> interface. The collection contains a list of <b>IFilterInfo</b> pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>
 

 

