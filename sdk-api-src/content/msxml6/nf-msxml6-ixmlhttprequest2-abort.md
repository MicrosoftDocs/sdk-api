---
UID: NF:msxml6.IXMLHTTPRequest2.Abort
title: IXMLHTTPRequest2::Abort (msxml6.h)
description: Cancels the current HTTP request.
helpviewer_keywords: ["Abort","Abort method [XMLHttpRequest2]","Abort method [XMLHttpRequest2]","IXMLHTTPRequest2 interface","IXMLHTTPRequest2 interface [XMLHttpRequest2]","Abort method","IXMLHTTPRequest2.Abort","IXMLHTTPRequest2::Abort","ixhr2.ixmlhttprequest2_abort","msxml6/IXMLHTTPRequest2::Abort"]
old-location: ixhr2\ixmlhttprequest2_abort.htm
tech.root: ixhr2
ms.assetid: B051D464-2328-44A2-A2BC-D0CDDCA79C64
ms.date: 12/05/2018
ms.keywords: Abort, Abort method [XMLHttpRequest2], Abort method [XMLHttpRequest2],IXMLHTTPRequest2 interface, IXMLHTTPRequest2 interface [XMLHttpRequest2],Abort method, IXMLHTTPRequest2.Abort, IXMLHTTPRequest2::Abort, ixhr2.ixmlhttprequest2_abort, msxml6/IXMLHTTPRequest2::Abort
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IXMLHTTPRequest2::Abort
 - msxml6/IXMLHTTPRequest2::Abort
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
 - IXMLHTTPRequest2.Abort
---

# IXMLHTTPRequest2::Abort


## -description

Cancels the current HTTP request.



## -returns

Returns <b>S_OK</b> on success.

## -remarks

After a request is aborted, the object representing the request is no longer valid.

This method is not guarantee to cancel a request. The app must still wait for to receive the <b>OnError</b> callback method that  indicates the request was  successfully aborted or the <b>OnResponseReceived</b> callback method that indicates the request was completed before the abort can be processed.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>
