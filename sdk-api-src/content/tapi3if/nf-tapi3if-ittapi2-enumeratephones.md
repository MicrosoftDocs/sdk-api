---
UID: NF:tapi3if.ITTAPI2.EnumeratePhones
title: ITTAPI2::EnumeratePhones
author: windows-sdk-content
description: The EnumeratePhones method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty enumeration and returns S_OK.
old-location: tapi3\ittapi2_enumeratephones.htm
tech.root: TAPI
ms.assetid: 6b6aba8d-fbf7-459f-9bc8-79647194b989
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EnumeratePhones, EnumeratePhones method [TAPI 2.2], EnumeratePhones method [TAPI 2.2],ITTAPI2 interface, ITTAPI2 interface [TAPI 2.2],EnumeratePhones method, ITTAPI2.EnumeratePhones, ITTAPI2::EnumeratePhones, _tapi3_ittapi2_enumeratephones, tapi3.ittapi2_enumeratephones, tapi3if/ITTAPI2::EnumeratePhones
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
 - ITTAPI2.EnumeratePhones
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI2::EnumeratePhones


## -description


The 
<b>EnumeratePhones</b> method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty enumeration and returns S_OK.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="https://msdn.microsoft.com/03fe03fc-c58d-4e2a-a187-5ab9a676e89e">get_Phones</a> method.


## -parameters




### -param ppEnumPhone [out]

Pointer to an 
<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a> interface returned by <b>ITTAPI2::EnumeratePhones</b>. The application must call <b>Release</b> on the 
<b>IEnumPhone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a>



<a href="https://msdn.microsoft.com/8c67f31e-783e-4371-9f17-063f8ecfc069">ITTAPI2</a>
 

 

