---
UID: NF:msxml6.IXMLHTTPRequest3.SetClientCertificate
title: IXMLHTTPRequest3::SetClientCertificate (msxml6.h)
description: Sets a client certificate to be used to authenticate against the URL specified in the Open method.
helpviewer_keywords: ["IXMLHTTPRequest3 interface [XMLHttpRequest2]","SetClientCertificate method","IXMLHTTPRequest3.SetClientCertificate","IXMLHTTPRequest3::SetClientCertificate","SetClientCertificate","SetClientCertificate method [XMLHttpRequest2]","SetClientCertificate method [XMLHttpRequest2]","IXMLHTTPRequest3 interface","ixhr2.ixmlhttprequest3_setclientcertificate","msxml6/IXMLHTTPRequest3::SetClientCertificate"]
old-location: ixhr2\ixmlhttprequest3_setclientcertificate.htm
tech.root: ixhr2
ms.assetid: fc3e2645-666c-42af-babd-1f476b6356b8
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest3 interface [XMLHttpRequest2],SetClientCertificate method, IXMLHTTPRequest3.SetClientCertificate, IXMLHTTPRequest3::SetClientCertificate, SetClientCertificate, SetClientCertificate method [XMLHttpRequest2], SetClientCertificate method [XMLHttpRequest2],IXMLHTTPRequest3 interface, ixhr2.ixmlhttprequest3_setclientcertificate, msxml6/IXMLHTTPRequest3::SetClientCertificate
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
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
 - IXMLHTTPRequest3::SetClientCertificate
 - msxml6/IXMLHTTPRequest3::SetClientCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest3.SetClientCertificate
---

# IXMLHTTPRequest3::SetClientCertificate


## -description

Sets a client certificate to be used to authenticate against the URL specified in the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-open">Open</a> method.

## -parameters

### -param cbClientCertificateHash [in]

The number of bytes of <i>pbClientCertHash</i> parameter.

### -param pbClientCertificateHash [in]

The thumbprint or hash completed over the complete client certificate being set on the HTTPS request.

### -param pwszPin [in]

This parameter is reserved.

## -returns

Returns S_OK on success.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-open">Open</a>