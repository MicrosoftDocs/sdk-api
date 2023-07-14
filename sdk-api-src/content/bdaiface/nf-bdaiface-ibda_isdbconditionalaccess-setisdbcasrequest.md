---
UID: NF:bdaiface.IBDA_ISDBConditionalAccess.SetIsdbCasRequest
title: IBDA_ISDBConditionalAccess::SetIsdbCasRequest (bdaiface.h)
description: Sends a conditional access system (CAS) command for Integrated Services Digital Broadcasting (ISDB).
helpviewer_keywords: ["IBDA_ISDBConditionalAccess interface [Microsoft TV Technologies]","SetIsdbCasRequest method","IBDA_ISDBConditionalAccess.SetIsdbCasRequest","IBDA_ISDBConditionalAccess::SetIsdbCasRequest","SetIsdbCasRequest","SetIsdbCasRequest method [Microsoft TV Technologies]","SetIsdbCasRequest method [Microsoft TV Technologies]","IBDA_ISDBConditionalAccess interface","bdaiface/IBDA_ISDBConditionalAccess::SetIsdbCasRequest","mstv.ibda_isdbconditionalaccess_setisdbcasrequest"]
old-location: mstv\ibda_isdbconditionalaccess_setisdbcasrequest.htm
tech.root: mstv
ms.assetid: c93351f5-1829-4405-b665-00f2e78391e0
ms.date: 12/05/2018
ms.keywords: IBDA_ISDBConditionalAccess interface [Microsoft TV Technologies],SetIsdbCasRequest method, IBDA_ISDBConditionalAccess.SetIsdbCasRequest, IBDA_ISDBConditionalAccess::SetIsdbCasRequest, SetIsdbCasRequest, SetIsdbCasRequest method [Microsoft TV Technologies], SetIsdbCasRequest method [Microsoft TV Technologies],IBDA_ISDBConditionalAccess interface, bdaiface/IBDA_ISDBConditionalAccess::SetIsdbCasRequest, mstv.ibda_isdbconditionalaccess_setisdbcasrequest
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
 - IBDA_ISDBConditionalAccess::SetIsdbCasRequest
 - bdaiface/IBDA_ISDBConditionalAccess::SetIsdbCasRequest
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
 - IBDA_ISDBConditionalAccess.SetIsdbCasRequest
---

# IBDA_ISDBConditionalAccess::SetIsdbCasRequest


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sends a conditional access system (CAS) command for Integrated Services Digital Broadcasting (ISDB).

## -parameters

### -param ulRequestId [in]

The numeric code for the CAS command. The ARIB standard defines these values. Enumeration constants for some commands are defined in the <a href="/previous-versions/windows/desktop/mstv/isdbcas-request-id">ISDBCAS_REQUEST_ID</a> enumeration.

### -param ulcbRequestBufferLen [in]

Size of the <i>pbRequestBuffer</i> array, in bytes.

### -param pbRequestBuffer [in]

Pointer to a byte array that contains the data for the command.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_isdbconditionalaccess">IBDA_ISDBConditionalAccess</a>