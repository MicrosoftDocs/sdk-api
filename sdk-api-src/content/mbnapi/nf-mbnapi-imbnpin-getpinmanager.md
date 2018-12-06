---
UID: NF:mbnapi.IMbnPin.GetPinManager
title: IMbnPin::GetPinManager
author: windows-sdk-content
description: Gets the IMbnPinManager.
old-location: mbn\imbnpin_getpinmanager.htm
tech.root: mbn
ms.assetid: 51957cb9-0204-4e07-aebf-1aaddb16b3c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPinManager, GetPinManager method [Microsoft Broadband Networks], GetPinManager method [Microsoft Broadband Networks],IMbnPin interface, IMbnPin interface [Microsoft Broadband Networks],GetPinManager method, IMbnPin.GetPinManager, IMbnPin::GetPinManager, mbn.imbnpin_getpinmanager, mbnapi/IMbnPin::GetPinManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnPin.GetPinManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnPin::GetPinManager


## -description


Gets the <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a>.


## -parameters




### -param pinManager [out]

Pointer to the address of an <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> to manage the PIN type.  When this function returns anything other than S_OK, this value is <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be used to retrieve an <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> interface for the given PIN type.  The <b>GetPinManager</b> method retrieves an <b>IMbnPinManager</b> interface from the <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> object passed in <a href="https://msdn.microsoft.com/4bdaa4e5-880e-4d1f-aec1-36811a0f21c1">IMbnPinEvents</a> methods.  




## -see-also




<a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a>
 

 

