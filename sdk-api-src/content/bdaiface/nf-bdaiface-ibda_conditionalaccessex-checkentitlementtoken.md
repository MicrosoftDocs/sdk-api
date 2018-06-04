---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IBDA_ConditionalAccessEx::CheckEntitlementToken


## -description


Checks the access availability of content that is identified by an entitlement token.

An <i>entitlement token</i> is a binary blob used to obtain access to a piece of content or to identify an event in a stream.


## -parameters




### -param ulDialogRequest [in]

A dialog request number that specifies the dialog that might be triggered by setting the value. A dialog is part of the device's user interface (MMI).


### -param bstrLanguage [in]

The language of the dialog. This string contains an ISO 639-2 language code with a dash followed by an ISO 3166 country/region code.


### -param RequestType [in]

The type of access that is being requested, specified as a member of the <a href="https://msdn.microsoft.com/b21bca45-e219-4670-b209-9d7a63fbd65c">BDA_CONDITIONALACCESS_REQUESTTYPE</a> enumeration.


### -param ulcbEntitlementTokenLen [in]

The size, in bytes, of the <i>pbEntitlementToken</i> array.


### -param pbEntitlementToken [in]

Pointer to a byte array that contains the entitlement token.


### -param pulDescrambleStatus [out]

Receives a status code indicating the descrambling status. For more information, see <i>Protected Broadcast Driver Architecture, Part 1: Core Services</i>, section 5.5. You can download this specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>. (This resource may not be available in some languages 

and countries.)


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9db9b6b1-fc4f-48f0-940e-d79a321ef094">IBDA_ConditionalAccessEx</a>
 

 

