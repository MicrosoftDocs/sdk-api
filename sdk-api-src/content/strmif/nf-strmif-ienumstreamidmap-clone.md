---
UID: NF:strmif.IEnumStreamIdMap.Clone
title: IEnumStreamIdMap::Clone
author: windows-sdk-content
description: The Clone method copies the collection.
old-location: dshow\ienumstreamidmap_clone.htm
old-project: DirectShow
ms.assetid: 2c6ef2a8-a5d7-434f-8de2-221502b7c5cf
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumStreamIdMap interface, IEnumStreamIdMap interface [DirectShow],Clone method, IEnumStreamIdMap.Clone, IEnumStreamIdMap::Clone, IEnumStreamIdMapClone, dshow.ienumstreamidmap_clone, strmif/IEnumStreamIdMap::Clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IEnumStreamIdMap::Clone


## -description



The <code>Clone</code> method copies the collection.




## -parameters




### -param ppIEnumStreamIdMap [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/8bca9255-2bc8-408b-9127-e3fe050fcf01">IEnumStreamIdMap</a> interface of the new collection object. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails,an <b>HRESULT</b> error code is returned.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8bca9255-2bc8-408b-9127-e3fe050fcf01">IEnumStreamIdMap Interface</a>
 

 

