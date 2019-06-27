---
UID: NF:strmif.ICaptureGraphBuilder2.FindPin
title: ICaptureGraphBuilder2::FindPin (strmif.h)
author: windows-sdk-content
description: The FindPin method retrieves a particular pin on a filter, or determines whether a given pin matches the specified criteria.
old-location: dshow\icapturegraphbuilder2_findpin.htm
tech.root: DirectShow
ms.assetid: f74e55d4-2d51-47a9-aca8-dd4e616a6253
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindPin, FindPin method [DirectShow], FindPin method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],FindPin method, ICaptureGraphBuilder2.FindPin, ICaptureGraphBuilder2::FindPin, ICaptureGraphBuilder2FindPin, dshow.icapturegraphbuilder2_findpin, strmif/ICaptureGraphBuilder2::FindPin
ms.topic: method
f1_keywords: 
 - "strmif/ICaptureGraphBuilder2.FindPin"
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
 - ICaptureGraphBuilder2.FindPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICaptureGraphBuilder2::FindPin


## -description



The <code>FindPin</code> method retrieves a particular pin on a filter, or determines whether a given pin matches the specified criteria.




## -parameters




### -param pSource [in]

Pointer to an interface on a filter, or to an interface on a pin.


### -param pindir [in]

Member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_pindirection">PIN_DIRECTION</a> enumeration that specifies the pin direction (input or output).


### -param pCategory [in]

A pointer to a GUID that specifies one of the pin categories listed in <a href="https://docs.microsoft.com/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>. To match any pin, regardless of category, set this parameter to <b>NULL</b>. 
          


### -param pType [in]

Pointer to a major type GUID that specifies the media type. Use <b>NULL</b> to match any media type.


### -param fUnconnected [in]

Boolean value that specifies whether the pin must be unconnected. If <b>TRUE</b>, the pin must be unconnected. If <b>FALSE</b>, the pin can be connected or unconnected.


### -param num [in]

Zero-based index of the pin to retrieve, from the set of matching pins. If <i>pSource</i> is a pointer to a filter, and more than one pin matches the search criteria, this parameter specifies which pin to retrieve. If <i>pSource</i> is a pointer to a pin, this parameter is ignored.


### -param ppPin [out]

Address of a pointer to receive the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of the matching pin.


## -returns



Returns S_OK if a matching pin is found, or E_FAIL otherwise.




## -remarks



If <i>pSource</i> is a pointer to a filter, the method searches for the <i>n</i>th pin on that filter that matches the search criteria, where <i>n</i> is given by the <i>num</i> parameter. If the method finds a matching pin, it returns a pointer to the pin in the <i>ppPin</i> parameter.

If <i>pSource</i> is a pointer to a pin, the method tests that pin against the search criteria. If the pin matches the criteria, the method returns S_OK, and returns a pointer to the pin's <b>IPin</b> interface in the <i>ppPin</i> parameter. Otherwise, it returns E_FAIL.

In either case, if the method succeeds, the <b>IPin</b> interface returned in the <i>ppPin</i> parameter has an outstanding reference count. Be sure to release the interface when you are done using it.

Typically, an application will not need to use this method. It is provided for unusually complex tasks, when the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-renderstream">ICaptureGraphBuilder2::RenderStream</a> method cannot build the filter graph. Use this method to retrieve a desired pin from a capture filter, and then build the rest of the graph manually.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>
 

 

