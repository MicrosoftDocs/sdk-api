---
UID: NF:strmif.IEnumStreamIdMap.Clone
title: IEnumStreamIdMap::Clone (strmif.h)
author: windows-sdk-content
description: The Clone method copies the collection.
old-location: dshow\ienumstreamidmap_clone.htm
tech.root: DirectShow
ms.assetid: 2c6ef2a8-a5d7-434f-8de2-221502b7c5cf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumStreamIdMap interface, IEnumStreamIdMap interface [DirectShow],Clone method, IEnumStreamIdMap.Clone, IEnumStreamIdMap::Clone, IEnumStreamIdMapClone, dshow.ienumstreamidmap_clone, strmif/IEnumStreamIdMap::Clone
ms.topic: method
f1_keywords: 
 - "strmif/IEnumStreamIdMap.Clone"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IEnumStreamIdMap.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumStreamIdMap::Clone


## -description



The <code>Clone</code> method copies the collection.




## -parameters




### -param ppIEnumStreamIdMap [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap</a> interface of the new collection object. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails,an <b>HRESULT</b> error code is returned.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap Interface</a>
 

 

