---
UID: NF:tapi3if.ITPhone.get_ButtonText
title: ITPhone::get_ButtonText
author: windows-sdk-content
description: The get_ButtonText method retrieves the button text associated with a particular button.
old-location: tapi3\itphone_get_buttontext.htm
tech.root: tapi
ms.assetid: 75a216fb-7bb3-4178-baa5-8ba478bd5422
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_ButtonText method, ITPhone.get_ButtonText, ITPhone::get_ButtonText, _tapi3_itphone_get_buttontext, get_ButtonText, get_ButtonText method [TAPI 2.2], get_ButtonText method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_buttontext, tapi3if/ITPhone::get_ButtonText
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
 - ITPhone.get_ButtonText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::get_ButtonText


## -description


The 
<b>get_ButtonText</b> method retrieves the button text associated with a particular button.

The application must call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails. See the TAPI 2.<i>x</i> documentation for more information about the concept of button text.


## -parameters




### -param lButtonID [in]

Button identifier.


### -param ppButtonText [out]

The <b>BSTR</b> representation of the button text. The <b>BSTR</b> is allocated using 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/b50427e9-94cd-47bb-910f-2f879df9bcf8">put_ButtonText</a>
 

 

