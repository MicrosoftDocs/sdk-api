---
UID: NF:strmif.IEnumStreamIdMap.Next
title: IEnumStreamIdMap::Next
author: windows-sdk-content
description: The Next method retrieves the next n elements in the collection.
old-location: dshow\ienumstreamidmap_next.htm
old-project: DirectShow
ms.assetid: 49e7ab23-e57e-4437-a195-88bccb6002de
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IEnumStreamIdMap interface [DirectShow],Next method, IEnumStreamIdMap.Next, IEnumStreamIdMap::Next, IEnumStreamIdMapNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumStreamIdMap interface, dshow.ienumstreamidmap_next, strmif/IEnumStreamIdMap::Next
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
 - IEnumStreamIdMap.Next
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IEnumStreamIdMap::Next


## -description



The <code>Next</code> method retrieves the next <i>n</i> elements in the collection.




## -parameters




### -param cRequest [in]

The number of elements to retrieve.


### -param pStreamIdMap [in, out]

Address of a user-allocated array containing <i>cRequest</i> elements that will receive the retrieved <a href="https://msdn.microsoft.com/75f41d9f-00a1-47e1-8b42-64de1e6abbdb">STREAM_ID_MAP</a> structures.


### -param pcReceived [out]

Receives the number of elements actually retrieved.


## -returns



Returns S_OK if successful. If the method fails,an <b>HRESULT</b> error code is returned.




## -remarks



If <i>cRequest</i> &gt;= 0 and <i>pcReceived</i> is not <b>NULL</b>, upon return <i>pcReceived</i> contains the number of stream ID maps remaining in the collection.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8bca9255-2bc8-408b-9127-e3fe050fcf01">IEnumStreamIdMap Interface</a>
 

 

