---
UID: NF:strmif.ISeekingPassThru.Init
title: ISeekingPassThru::Init
author: windows-sdk-content
description: The Init method initializes the seeking helper object.
old-location: dshow\iseekingpassthru_init.htm
tech.root: DirectShow
ms.assetid: bb32c20c-bbae-403a-885b-f07c6dcf46f4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ISeekingPassThru interface [DirectShow],Init method, ISeekingPassThru.Init, ISeekingPassThru::Init, ISeekingPassThruInit, Init, Init method [DirectShow], Init method [DirectShow],ISeekingPassThru interface, dshow.iseekingpassthru_init, strmif/ISeekingPassThru::Init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISeekingPassThru.Init
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
- ISeekingPassThru.Init
: 
---

# ISeekingPassThru::Init


## -description



The <code>Init</code> method initializes the seeking helper object.




## -parameters




### -param bSupportRendering [in]

Boolean value that specifies whether the filter is a renderer. Use the value <b>TRUE</b> if the filter is a renderer, or <b>FALSE</b> otherwise.


### -param pPin [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface on the input pin of the filter.


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Object was already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to create the object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a22f2723-b44e-4c7e-8508-db5c6af5b1d6">ISeekingPassThru Interface</a>
 

 

