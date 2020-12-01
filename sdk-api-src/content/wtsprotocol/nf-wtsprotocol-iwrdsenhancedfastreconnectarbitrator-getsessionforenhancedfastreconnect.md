---
UID: NF:wtsprotocol.IWRdsEnhancedFastReconnectArbitrator.GetSessionForEnhancedFastReconnect
title: IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect (wtsprotocol.h)
description: Protocol stack uses this method to return Session ID to be used for Enhanced Fast Reconnect.
helpviewer_keywords: ["GetSessionForEnhancedFastReconnect","GetSessionForEnhancedFastReconnect method [Remote Desktop Services]","GetSessionForEnhancedFastReconnect method [Remote Desktop Services]","IWRdsEnhancedFastReconnectArbitrator interface","IWRdsEnhancedFastReconnectArbitrator interface [Remote Desktop Services]","GetSessionForEnhancedFastReconnect method","IWRdsEnhancedFastReconnectArbitrator.GetSessionForEnhancedFastReconnect","IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect","termserv.iwrdsenhancedfastreconnectarbitrator_getsessionforenhancedfastreconnect","wtsprotocol/IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect"]
old-location: termserv\iwrdsenhancedfastreconnectarbitrator_getsessionforenhancedfastreconnect.htm
tech.root: TermServ
ms.assetid: 1b936827-421e-49e6-87f6-3932ea673c68
ms.date: 11/02/2020
ms.keywords: GetSessionForEnhancedFastReconnect, EnableWddGetSessionForEnhancedFastReconnectmIdd method [Remote Desktop Services], GetSessionForEnhancedFastReconnect method [Remote Desktop Services], IWRdsEnhancedFastReconnectArbitrator interface, IWRdsEnhancedFastReconnectArbitrator interface [Remote Desktop Services], GetSessionForEnhancedFastReconnect method, IWRdsEnhancedFastReconnectArbitrator.GetSessionForEnhancedFastReconnect, IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect, termserv.iwrdsenhancedfastreconnectarbitrator_getsessionforenhancedfastreconnect, wtsprotocol/IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect
req.header: wtsprotocol.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 21H1
f1_keywords:
 - IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect
 - wtsprotocol/IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWRdsEnhancedFastReconnectArbitrator.GetSessionForEnhancedFastReconnect
---

# IWRdsEnhancedFastReconnectArbitrator::GetSessionForEnhancedFastReconnect


## -description

Protocol stack uses this method to return the Session ID to be used for Enhanced Fast Reconnect.

## -parameters

### -param pSessionIdArray [in]

Array of Session IDs matching the enhanced fast reconnect criteria

### -param dwSessionCount [in]

Size of Session ID array (in elements)

### -param pResultSessionId [out]

Pointer to LONG variable to receive the resultant Session ID

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsenhancedfastreconnectarbitrator">IWRdsEnhancedFastReconnectArbitrator</a>

