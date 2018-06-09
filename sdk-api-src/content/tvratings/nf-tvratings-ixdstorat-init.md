---
UID: NF:tvratings.IXDSToRat.Init
title: IXDSToRat::Init
author: windows-sdk-content
description: The Init method sets the XDSToRat object to its initial state.
old-location: mstv\ixdstorat_init.htm
old-project: mstv
ms.assetid: c7c38755-46d3-4100-ba14-c153c4a6a517
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IXDSToRat interface [Microsoft TV Technologies],Init method, IXDSToRat.Init, IXDSToRat::Init, IXDSToRatInit, Init, Init method [Microsoft TV Technologies], Init method [Microsoft TV Technologies],IXDSToRat interface, mstv.ixdstorat_init, tvratings/IXDSToRat::Init
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: EnTvRat_US_TV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tvratings.h
api_name:
 - IXDSToRat.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IXDSToRat::Init


## -description


The <b>Init</b> method sets the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object to its initial state.


## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The XDS Codec filter calls this method on startup or after a discontinuity, such as a channel change. The <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object should clear any internal buffers and reset its parsing state. This method prevents decoding errors caused by channel changes or other interruptions.




## -see-also




<a href="https://msdn.microsoft.com/de65e5cd-3f4b-4925-a6b8-636fc2e332ec">IXDSToRat Interface</a>
 

 

