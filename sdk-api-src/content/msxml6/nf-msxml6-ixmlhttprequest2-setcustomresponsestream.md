---
UID: NF:msxml6.IXMLHTTPRequest2.SetCustomResponseStream
title: IXMLHTTPRequest2::SetCustomResponseStream
author: windows-sdk-content
description: Provides a custom stream to replace the standard stream for receiving an HTTP response.
old-location: ixhr2\ixmlhttprequest2_setcustomresponsestream.htm
old-project: ixhr2
ms.assetid: 64341C82-85EC-402F-A875-85706DFD7B25
ms.author: windowssdkdev
ms.date: 04/02/2018
ms.keywords: IXMLHTTPRequest2 interface [XMLHttpRequest2],SetCustomResponseStream method, IXMLHTTPRequest2.SetCustomResponseStream, IXMLHTTPRequest2::SetCustomResponseStream, SetCustomResponseStream, SetCustomResponseStream method [XMLHttpRequest2], SetCustomResponseStream method [XMLHttpRequest2],IXMLHTTPRequest2 interface, ixhr2.ixmlhttprequest2_setcustomresponsestream, msxml6/IXMLHTTPRequest2::SetCustomResponseStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XHR_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msxml6.h
api_name:
-	IXMLHTTPRequest2.SetCustomResponseStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest2::SetCustomResponseStream


## -description


Provides a custom stream to replace the standard stream for receiving an HTTP response.


## -parameters




### -param pSequentialStream

Custom stream that will receive the HTTP response. <a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream</a>



## -returns



Returns <b>S_OK</b> on success.




## -remarks



After this method is called, <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> will call the <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> method when it receives response data from the server. You can begin processing the data at that time, but avoid heavy processing because the call is made inline to receiving further data from the server. Because this <b>IXMLHTTPRequest2</b> never calls <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> on the custom stream, it is safe to return <b>E_NOTIMPL</b> if the application does not need to use <b>ISequentialStream::Read</b>.




## -see-also




<a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream Interface</a>



<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>
 

 

