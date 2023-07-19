---
UID: NF:bdaiface.IBDA_ConditionalAccessEx.CheckEntitlementToken
title: IBDA_ConditionalAccessEx::CheckEntitlementToken (bdaiface.h)
description: Checks the access availability of content that is identified by an entitlement token.
helpviewer_keywords: ["CheckEntitlementToken","CheckEntitlementToken method [Microsoft TV Technologies]","CheckEntitlementToken method [Microsoft TV Technologies]","IBDA_ConditionalAccessEx interface","IBDA_ConditionalAccessEx interface [Microsoft TV Technologies]","CheckEntitlementToken method","IBDA_ConditionalAccessEx.CheckEntitlementToken","IBDA_ConditionalAccessEx::CheckEntitlementToken","bdaiface/IBDA_ConditionalAccessEx::CheckEntitlementToken","mstv.ibda_conditionalaccessex_checkentitlementtoken"]
old-location: mstv\ibda_conditionalaccessex_checkentitlementtoken.htm
tech.root: mstv
ms.assetid: ea581065-b10b-4a2a-9090-99d6fd140ea9
ms.date: 12/05/2018
ms.keywords: CheckEntitlementToken, CheckEntitlementToken method [Microsoft TV Technologies], CheckEntitlementToken method [Microsoft TV Technologies],IBDA_ConditionalAccessEx interface, IBDA_ConditionalAccessEx interface [Microsoft TV Technologies],CheckEntitlementToken method, IBDA_ConditionalAccessEx.CheckEntitlementToken, IBDA_ConditionalAccessEx::CheckEntitlementToken, bdaiface/IBDA_ConditionalAccessEx::CheckEntitlementToken, mstv.ibda_conditionalaccessex_checkentitlementtoken
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_ConditionalAccessEx::CheckEntitlementToken
 - bdaiface/IBDA_ConditionalAccessEx::CheckEntitlementToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_ConditionalAccessEx.CheckEntitlementToken
---

# IBDA_ConditionalAccessEx::CheckEntitlementToken


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Checks the access availability of content that is identified by an entitlement token.

An <i>entitlement token</i> is a binary blob used to obtain access to a piece of content or to identify an event in a stream.

## -parameters

### -param ulDialogRequest [in]

A dialog request number that specifies the dialog that might be triggered by setting the value. A dialog is part of the device's user interface (MMI).

### -param bstrLanguage [in]

The language of the dialog. This string contains an ISO 639-2 language code with a dash followed by an ISO 3166 country/region code.

### -param RequestType [in]

The type of access that is being requested, specified as a member of the <a href="/previous-versions/windows/desktop/mstv/bda-conditionalaccess-requesttype">BDA_CONDITIONALACCESS_REQUESTTYPE</a> enumeration.

### -param ulcbEntitlementTokenLen [in]

The size, in bytes, of the <i>pbEntitlementToken</i> array.

### -param pbEntitlementToken [in]

Pointer to a byte array that contains the entitlement token.

### -param pulDescrambleStatus [out]

Receives a status code indicating the descrambling status. For more information, see <i>Protected Broadcast Driver Architecture, Part 1: Core Services</i>, section 5.5.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_conditionalaccessex">IBDA_ConditionalAccessEx</a>