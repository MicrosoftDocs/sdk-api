---
UID: NF:msxml6.IXMLHTTPRequest2.Abort
title: IXMLHTTPRequest2::Abort
author: windows-sdk-content
description: Cancels the current HTTP request.
old-location: ixhr2\ixmlhttprequest2_abort.htm
tech.root: ixhr2
ms.assetid: B051D464-2328-44A2-A2BC-D0CDDCA79C64
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Abort, Abort method [XMLHttpRequest2], Abort method [XMLHttpRequest2],IXMLHTTPRequest2 interface, IXMLHTTPRequest2 interface [XMLHttpRequest2],Abort method, IXMLHTTPRequest2.Abort, IXMLHTTPRequest2::Abort, ixhr2.ixmlhttprequest2_abort, msxml6/IXMLHTTPRequest2::Abort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2.Abort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXMLHTTPRequest2::Abort


## -description


Cancels the current HTTP request.


## -parameters






## -returns



Returns <b>S_OK</b> on success.




## -remarks



After a request is aborted, the object representing the request is no longer valid.

This method is not guarantee to cancel a request. The app must still wait for to receive the <b>OnError</b> callback method that  indicates the request was  successfully aborted or the <b>OnResponseReceived</b> callback method that indicates the request was completed before the abort can be processed.




## -see-also




<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>
 

 

