---
UID: NF:dinputd.IDirectInputJoyConfig8.SetCooperativeLevel
title: IDirectInputJoyConfig8::SetCooperativeLevel (dinputd.h)
author: windows-sdk-content
description: The IDirectInputJoyConfig8::SetCooperativeLevel method establishes the cooperation level for the instance of the device. The only cooperative levels supported for the IDirectInputJoyConfig8 interface are DISCL_EXCLUSIVE and DISCL_BACKGROUND.
old-location: hid\idirectinputjoyconfig8_setcooperativelevel.htm
tech.root: hid
ms.assetid: 0132194a-ee7b-4aa2-af79-f92071072429
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],SetCooperativeLevel method, IDirectInputJoyConfig8.SetCooperativeLevel, IDirectInputJoyConfig8::SetCooperativeLevel, SetCooperativeLevel, SetCooperativeLevel method [Human Input Devices], SetCooperativeLevel method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_3730e9ce-af55-43a3-866f-ecb288958005.xml, dinputd/IDirectInputJoyConfig8::SetCooperativeLevel, hid.idirectinputjoyconfig8_setcooperativelevel
ms.topic: method
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputJoyConfig8.SetCooperativeLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectInputJoyConfig8::SetCooperativeLevel


## -description


The <b>IDirectInputJoyConfig8::SetCooperativeLevel </b>method establishes the cooperation level for the instance of the device. The only cooperative levels supported for the <b>IDirectInputJoyConfig8</b> interface are DISCL_EXCLUSIVE and DISCL_BACKGROUND. 


## -parameters




### -param arg1

Handle to the window associated with the interface. This parameter must be non-NULL and must be a top-level window. It is an error to destroy the window while it is still associated with an <b>IDirectInputJoyConfig8</b> interface. 


### -param arg2

Specifies one of a set of flags that describe the  level of cooperation associated with the device. The value must be DISCL_EXCLUSIVE | DISCL_BACKGROUND. 


## -returns



Returns DI_OK if successful; otherwise, returns the following COM error value (this value is intended to be illustrative and is not necessarily comprehensive): 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDPARAM </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid. 

</td>
</tr>
</table>
 



