---
UID: NF:bdaiface.IBDA_ConditionalAccessEx.CheckEntitlementToken
title: IBDA_ConditionalAccessEx::CheckEntitlementToken
author: windows-sdk-content
description: Checks the access availability of content that is identified by an entitlement token.
old-location: mstv\ibda_conditionalaccessex_checkentitlementtoken.htm
old-project: mstv
ms.assetid: ea581065-b10b-4a2a-9090-99d6fd140ea9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CheckEntitlementToken, CheckEntitlementToken method [Microsoft TV Technologies], CheckEntitlementToken method [Microsoft TV Technologies],IBDA_ConditionalAccessEx interface, IBDA_ConditionalAccessEx interface [Microsoft TV Technologies],CheckEntitlementToken method, IBDA_ConditionalAccessEx.CheckEntitlementToken, IBDA_ConditionalAccessEx::CheckEntitlementToken, bdaiface/IBDA_ConditionalAccessEx::CheckEntitlementToken, mstv.ibda_conditionalaccessex_checkentitlementtoken
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_ConditionalAccessEx.CheckEntitlementToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

