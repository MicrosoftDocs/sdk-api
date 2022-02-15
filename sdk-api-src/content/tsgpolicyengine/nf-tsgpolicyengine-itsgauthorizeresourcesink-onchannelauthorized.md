---
UID: NF:tsgpolicyengine.ITSGAuthorizeResourceSink.OnChannelAuthorized
title: ITSGAuthorizeResourceSink::OnChannelAuthorized (tsgpolicyengine.h)
description: Notifies Remote Desktop Gateway (RD Gateway) about the result of an attempt to authorize a resource.
helpviewer_keywords: ["ITSGAuthorizeResourceSink interface [Remote Desktop Services]","OnChannelAuthorized method","ITSGAuthorizeResourceSink.OnChannelAuthorized","ITSGAuthorizeResourceSink::OnChannelAuthorized","OnChannelAuthorized","OnChannelAuthorized method [Remote Desktop Services]","OnChannelAuthorized method [Remote Desktop Services]","ITSGAuthorizeResourceSink interface","termserv.itsgauthorizeresourcesink_onchannelauthorized","tsgpolicyengine/ITSGAuthorizeResourceSink::OnChannelAuthorized"]
old-location: termserv\itsgauthorizeresourcesink_onchannelauthorized.htm
tech.root: TermServ
ms.assetid: e09247af-54ea-4846-97d5-d503a811ab29
ms.date: 12/05/2018
ms.keywords: ITSGAuthorizeResourceSink interface [Remote Desktop Services],OnChannelAuthorized method, ITSGAuthorizeResourceSink.OnChannelAuthorized, ITSGAuthorizeResourceSink::OnChannelAuthorized, OnChannelAuthorized, OnChannelAuthorized method [Remote Desktop Services], OnChannelAuthorized method [Remote Desktop Services],ITSGAuthorizeResourceSink interface, termserv.itsgauthorizeresourcesink_onchannelauthorized, tsgpolicyengine/ITSGAuthorizeResourceSink::OnChannelAuthorized
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
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
 - ITSGAuthorizeResourceSink::OnChannelAuthorized
 - tsgpolicyengine/ITSGAuthorizeResourceSink::OnChannelAuthorized
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGAuthorizeResourceSink.OnChannelAuthorized
---

# ITSGAuthorizeResourceSink::OnChannelAuthorized


## -description

Notifies Remote Desktop Gateway (RD Gateway) about the result of an  attempt to authorize a resource.

## -parameters

### -param hrIn [in]

The result of the authorization attempt. Specify <b>S_OK</b> to indicate that the attempt succeeded. Specify any other value to indicate that the attempt failed.

### -param mainSessionId [in]

A unique identifier assigned to the connection request by RD Gateway.

### -param subSessionId [in]

A unique identifier assigned to the subsession by RD Gateway. A subsession is a session launched from another session.

### -param allowedResourceNames [in]

A pointer to a <b>BSTR</b> that contains a list of resources that were successfully authorized.

### -param numAllowedResourceNames [in]

The number of resources referenced by the <i>allowedResourceNames</i> parameter. If the function succeeds, this parameter must be one or more.

### -param failedResourceNames [in]

A pointer to a <b>BSTR</b> that contains a list of resources that failed authorization.

### -param numFailedResourceNames [in]

The number of resources referenced by the <i>failedResourceNames</i> parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can call this method from your implementation of 
    <a href="/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-authorizeresource">AuthorizeResource</a>. If 
    authorization requires more than 1 second, we recommend launching a separate thread to perform 
    authentication.


For a sample that uses the <b>OnChannelAuthorized</b> method, see the [Remote Desktop Gateway Pluggable Authentication and Authorization](https://github.com/microsoftarchive/msdn-code-gallery-community-m-r/tree/master/Remote%20Desktop%20Gateway%20Pluggable%20Authentication%20and%20Authorization%20Sample) sample.

## -see-also

<a href="/windows/desktop/api/tsgpolicyengine/nn-tsgpolicyengine-itsgauthorizeresourcesink">ITSGAuthorizeResourceSink</a>