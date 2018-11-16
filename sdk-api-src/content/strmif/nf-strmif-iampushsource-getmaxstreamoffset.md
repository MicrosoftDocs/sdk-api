---
UID: NF:strmif.IAMPushSource.GetMaxStreamOffset
title: IAMPushSource::GetMaxStreamOffset
author: windows-sdk-content
description: The GetMaxStreamOffset method retrieves the maximum stream offset the filter can support.
old-location: dshow\iampushsource_getmaxstreamoffset.htm
tech.root: DirectShow
ms.assetid: 503ec642-0a86-47b9-b453-08ab90346630
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetMaxStreamOffset, GetMaxStreamOffset method [DirectShow], GetMaxStreamOffset method [DirectShow],IAMPushSource interface, IAMPushSource interface [DirectShow],GetMaxStreamOffset method, IAMPushSource.GetMaxStreamOffset, IAMPushSource::GetMaxStreamOffset, IAMPushSourceGetMaxStreamOffset, dshow.iampushsource_getmaxstreamoffset, strmif/IAMPushSource::GetMaxStreamOffset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAMPushSource.GetMaxStreamOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMPushSource.GetMaxStreamOffset
: 
---

# IAMPushSource::GetMaxStreamOffset


## -description



The <code>GetMaxStreamOffset</code> method retrieves the maximum stream offset the filter can support.




## -parameters




### -param prtMaxOffset [out]

Pointer to a variable that receives a reference time indicating the maximum offset the filter can support.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns E_POINTER or S_OK.




## -remarks



If the stream offset is set to a value larger than the maximum supported offset, the filter is not guaranteed to have a buffer large enough to hold data for the entire amount of the offset. Unless there is another buffer downstream, data might be lost.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5ab294a8-f250-405c-a589-68998bc04cdf">IAMPushSource Interface</a>
 

 

