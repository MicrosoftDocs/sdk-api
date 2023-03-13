---
UID: NF:wtsprotocol.IWRdsEnhancedFastReconnectArbitrator.GetSessionForEnhancedFastReconnect
tech.root: TermServ
title: IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect
ms.date: 06/09/2021
ms.topic: language-reference
targetos: Windows
description: The protocol stack uses this method to return the session ID to be used for enhanced fast reconnect.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wtsprotocol.h
req.idl: Wtsprotocol.idl
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2022
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect
f1_keywords:
 - IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect
 - wtsprotocol/IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect
dev_langs:
 - c++
---

## -description

The protocol stack uses this method to return the session ID to be used for enhanced fast reconnect.

## -parameters

### -param pSessionIdArray

An array of session IDs that match the enhanced fast reconnect criteria.

### -param dwSessionCount

The size of the *pSessionIdArray* array (in elements).

### -param pResultSessionId

Pointer to LONG variable to receive the resultant session ID.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsenhancedfastreconnectarbitrator">IWRdsEnhancedFastReconnectArbitrator</a>
