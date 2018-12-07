---
UID: NF:tapi3if.ITPhone.get_Privilege
title: ITPhone::get_Privilege
author: windows-sdk-content
description: The get_Privilege method retrieves the privilege of the open phone.
old-location: tapi3\itphone_get_privilege.htm
tech.root: tapi
ms.assetid: 88103a48-a5cd-43a7-a88e-9b16313b35c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Privilege method, ITPhone.get_Privilege, ITPhone::get_Privilege, _tapi3_itphone_get_privilege, get_Privilege, get_Privilege method [TAPI 2.2], get_Privilege method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_privilege, tapi3if/ITPhone::get_Privilege
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
 - ITPhone.get_Privilege
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::get_Privilege


## -description


The 
<b>get_Privilege</b> method retrieves the privilege of the open phone.

The application must call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param pPrivilege [out]

The 
<a href="https://msdn.microsoft.com/f1c162c6-058d-4cf2-a493-17b7752ffeeb">PHONE_PRIVILEGE</a> descriptor for the application's privilege status with respect to the phone device.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>
 

 

