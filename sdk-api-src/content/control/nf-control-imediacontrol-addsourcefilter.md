---
UID: NF:control.IMediaControl.AddSourceFilter
title: IMediaControl::AddSourceFilter method
author: windows-driver-content
description: The AddSourceFilter method adds a source filter to the filter graph.
old-location: dshow\imediacontrol_addsourcefilter.htm
old-project: DirectShow
ms.assetid: b0d59a47-23a7-4e59-adfa-e01945a5d014
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: AddSourceFilter method [DirectShow], AddSourceFilter method [DirectShow], IMediaControl interface, AddSourceFilter,IMediaControl.AddSourceFilter, IMediaControl, IMediaControl interface [DirectShow], AddSourceFilter method, IMediaControl::AddSourceFilter, IMediaControlAddSourceFilter, control/IMediaControl::AddSourceFilter, dshow.imediacontrol_addsourcefilter
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaControl.AddSourceFilter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaControl::AddSourceFilter method


## -description



The <code>AddSourceFilter</code> method adds a source filter to the filter graph.



This method is intended for use by Visual Basic 6.0 applications. It was documented for Visual Basic 6.0 as the <b>FilgraphManager.AddSourceFilter</b> method. C++ applications should use the <a href="https://msdn.microsoft.com/ed4d7fc6-558b-474f-ae8d-58aa8479b4d2">IGraphBuilder::AddSourceFilter</a> method instead.


## -parameters




### -param strFilename [in]

Specifies the name of the file to load.


### -param ppUnk [out]

Receives a pointer to the <b>IDispatch</b> interface.  The caller must release the interface. You can query the returned pointer for the <b>IFilterInfo</b> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl Interface</a>
 

 

