---
UID: NF:control.IMediaControl.get_RegFilterCollection
title: IMediaControl::get_RegFilterCollection
author: windows-sdk-content
description: The get_RegFilterCollection method retrieves a collection of all the filters listed in the registry.
old-location: dshow\imediacontrol_get_regfiltercollection.htm
tech.root: DirectShow
ms.assetid: 55257cef-2777-4a88-8805-e474e3b13c75
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMediaControl interface [DirectShow],get_RegFilterCollection method, IMediaControl.get_RegFilterCollection, IMediaControl::get_RegFilterCollection, IMediaControlget_RegFilterCollection, control/IMediaControl::get_RegFilterCollection, dshow.imediacontrol_get_regfiltercollection, get_RegFilterCollection, get_RegFilterCollection method [DirectShow], get_RegFilterCollection method [DirectShow],IMediaControl interface
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
 - IMediaControl.get_RegFilterCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- control.h
: 
- IMediaControl.get_RegFilterCollection
: 
---

# IMediaControl::get_RegFilterCollection


## -description



The <code>get_RegFilterCollection</code> method retrieves a collection of all the filters listed in the registry.



This method is intended for use by Visual Basic 6.0 applications. It was documented for Visual Basic 6.0 as the <b>FilgraphManager.RegFilterCollection</b> property. C++ applications should use the <a href="https://msdn.microsoft.com/f121b4c3-fce1-4be3-ace4-5084242130f6">IFilterMapper2::EnumMatchingFilters</a> method instead.


## -parameters




### -param ppUnk [out]

Receives a pointer to the <b>IDispatch</b> interface.  The caller must release the interface. You can query the returned pointer for the <b>IAMCollection</b> interface. The collection contains a list of <b>IRegFilterInfo</b> pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl Interface</a>
 

 

