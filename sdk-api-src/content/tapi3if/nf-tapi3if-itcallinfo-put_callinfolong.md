---
UID: NF:tapi3if.ITCallInfo.put_CallInfoLong
title: ITCallInfo::put_CallInfoLong
author: windows-driver-content
description: The put_CallInfoLong method sets call information items described by a long, such as the bearer mode.
old-location: tapi3\itcallinfo_put_callinfolong.htm
old-project: Tapi
ms.assetid: b5198b78-56f7-4964-970a-1068f2db4743
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],put_CallInfoLong method, ITCallInfo.put_CallInfoLong, ITCallInfo::put_CallInfoLong, _tapi3_itcallinfo_put_callinfolong, put_CallInfoLong, put_CallInfoLong method [TAPI 2.2], put_CallInfoLong method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_put_callinfolong, tapi3if/ITCallInfo::put_CallInfoLong
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITCallInfo.put_CallInfoLong
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallInfo::put_CallInfoLong


## -description


The 
<b>put_CallInfoLong</b> method sets call information items described by a long, such as the bearer mode.


## -parameters




### -param CallInfoLong [in]


<a href="https://msdn.microsoft.com/48a27ba2-e21d-46bb-8fba-8052fc68b851">CALLINFO_LONG</a> indicator of information type needed, such as CIL_BEARERMODE.


### -param lCallInfoLongVal [in]

Pointer to new value.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>CallInfoLong</i> parameter is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The current 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a> is not valid for this operation.
								

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/48a27ba2-e21d-46bb-8fba-8052fc68b851">CALLINFO_LONG</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/0c00e672-7bad-4a44-a76a-efd222f763d7">get_CallInfoLong</a>
 

 

