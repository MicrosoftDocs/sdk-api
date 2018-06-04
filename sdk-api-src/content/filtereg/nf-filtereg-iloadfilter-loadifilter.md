---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ILoadFilter::LoadIFilter


## -description


Retrieves and loads the most appropriate filter that is mapped to a Shell data source.



## -parameters




### -param pwcsPath [in]

Pointer to a comma-delimited null-terminated Unicode string buffer that specifies the path of the file to be filtered. This parameter can be null.


### -param pFilteredSources [in]

Pointer to the <a href="https://msdn.microsoft.com/5baae290-aead-4986-a7d4-0302931e0104">FILTERED_DATA_SOURCES</a> structure that specifies parameters for a Shell data source for which a filter is loaded. This parameter cannot be null.


### -param pUnkOuter [in]

If the object is being created as part of an aggregate, specify a pointer to the controlling <a href="http://msdn.microsoft.com/en-us/library/dd757099(VS.85).aspx">IUnknown</a> interface of the aggregate.


### -param fUseDefault [in]

If <b>TRUE</b>, use the default filter; if <b>FALSE</b>, proceed with the most appropriate filter that is available.


### -param pFilterClsid [in, out]

Pointer to the CLSID (CLSID_FilterRegistration) that receives the class identifier of the returned filter.


### -param SearchDecSize [in, out]

Not implemented.


### -param pwcsSearchDesc [in, out]

Not implemented.


### -param ppIFilt [in, out]

The address of a pointer to an implementation of an <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface that <b>LoadIFilter</b> selects. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A filter, also known as a filter handler, is an implementation of the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface.

<b>ILoadFilter</b> attempts to load a filter that can process a Shell data source of the type specified in the <i>pFilteredSources</i> parameter through the <i>pwcsPath</i> parameter.

If an appropriate filter for the data source is not found, and <i>fUseDefault</i> is <b>false</b>, this method returns null in the <i>ppIFilt</i> parameter. If an appropriate filter for the data source is not found, and <i>fUseDefault</i> is <b>true</b>, the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface on the default <b>IFilter</b> is returned in the <i>ppIFilt</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/7ac51909-fa0e-4f97-8da0-0ab4c5de7d60">ILoadFilter</a>
 

 

