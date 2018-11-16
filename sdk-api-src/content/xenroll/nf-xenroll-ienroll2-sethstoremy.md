---
UID: NF:xenroll.IEnroll2.SetHStoreMy
title: IEnroll2::SetHStoreMy
author: windows-sdk-content
description: The SetHStoreMy method specifies the handle to use for the MY store. This method was first defined in the IEnroll2 interface.
old-location: security\ienroll4_sethstoremy.htm
tech.root: SecCrypto
ms.assetid: 669c8fe4-def3-41c5-82fc-95c26f3950c8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnroll interface [Security],SetHStoreMy method, IEnroll2 interface [Security],SetHStoreMy method, IEnroll2.SetHStoreMy, IEnroll2::SetHStoreMy, IEnroll::SetHStoreMy, SetHStoreMy, SetHStoreMy method [Security], SetHStoreMy method [Security],IEnroll interface, SetHStoreMy method [Security],IEnroll2 interface, security.ienroll4_sethstoremy, xenroll/IEnroll2::SetHStoreMy, xenroll/IEnroll::SetHStoreMy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.SetHStoreMy
 - IEnroll2.SetHStoreMy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xenroll.h
: 
- IEnroll2.SetHStoreMy
: 
---

# IEnroll2::SetHStoreMy


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SetHStoreMy</b> method specifies the handle to use for the MY store. This method was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.


## -parameters




### -param hStore [in]

Certificate store handle to use for the MY store.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>



<a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a>
 

 

