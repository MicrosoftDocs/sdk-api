---
UID: NF:tapi3if.ITPhone.put_LampMode
title: ITPhone::put_LampMode
author: windows-sdk-content
description: The put_LampMode method sets the current lamp mode for the given lamp.
old-location: tapi3\itphone_put_lampmode.htm
tech.root: tapi
ms.assetid: 0445cf2c-1b00-4136-bdab-3c6e0669ef11
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_LampMode method, ITPhone.put_LampMode, ITPhone::put_LampMode, _tapi3_itphone_put_lampmode, put_LampMode, put_LampMode method [TAPI 2.2], put_LampMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_lampmode, tapi3if/ITPhone::put_LampMode
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhone.put_LampMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::put_LampMode


## -description


The 
<b>put_LampMode</b> method sets the current lamp mode for the given lamp.


## -parameters




### -param lLampID [in]

Lamp identifier.


### -param LampMode [in]

The 
<a href="https://msdn.microsoft.com/cb971936-269c-4e59-bfc1-a3edc977ceb5">PHONE_LAMP_MODE</a> descriptor for the phone's lamp status.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/5e0fa135-304a-4598-a6cd-2e5734b3678c">get_LampMode</a>
 

 

