---
UID: NF:tuner.IESRequestTunerEvent.GetReason
title: IESRequestTunerEvent::GetReason (tuner.h)
author: windows-sdk-content
description: Gets a code that indicates the reason a device is requesting exclusive access to a tuner and its Conditional Access Services (CAS).
old-location: mstv\iesrequesttunerevent_getreason.htm
tech.root: mstv
ms.assetid: ff8b9080-0299-4ba9-a49d-9ef142e91eb8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetReason, GetReason method [Microsoft TV Technologies], GetReason method [Microsoft TV Technologies],IESRequestTunerEvent interface, IESRequestTunerEvent interface [Microsoft TV Technologies],GetReason method, IESRequestTunerEvent.GetReason, IESRequestTunerEvent::GetReason, mstv.iesrequesttunerevent_getreason, tuner/IESRequestTunerEvent::GetReason
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESRequestTunerEvent.GetReason
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESRequestTunerEvent::GetReason


## -description


Gets a code that indicates the reason a device is requesting exclusive access to a tuner and its Conditional Access Services (CAS).


## -parameters




### -param pbyReason [out, retval]

Gets a 1-byte code that indicates the reason for the request.  The code can be any of the following values.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x00</b></dt>
</dl>
</td>
<td width="60%">
Unspecified.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x01</b></dt>
</dl>
</td>
<td width="60%">
The requesting device needs the tuner to download an internal update, such as new firmware.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>[Other]</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da1183a3-6f31-402a-b103-448cf13705a9">IESRequestTunerEvent</a>
 

 

