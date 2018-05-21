---
UID: NF:webservices.WsEndWriterCanonicalization
title: WsEndWriterCanonicalization function
author: windows-driver-content
description: This function stops XML canonicalization started by the preceding WsStartWriterCanonicalization call. Remaining canonical bytes buffered by the writer are written to the callback function.
old-location: wsw\wsendwritercanonicalization.htm
old-project: wsw
ms.assetid: 169f971e-0cd2-44e7-81fc-059cc3cd357d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WsEndWriterCanonicalization, WsEndWriterCanonicalization function [Web Services for Windows], webservices/WsEndWriterCanonicalization, wsw.wsendwritercanonicalization
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsEndWriterCanonicalization
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsEndWriterCanonicalization function


## -description



        This function stops XML canonicalization started by the preceding <a href="https://msdn.microsoft.com/e9ea26d6-a136-4103-ac67-42e943ea67b5">WsStartWriterCanonicalization</a> call.
      Remaining canonical bytes buffered by the writer are written to the callback function.


## -parameters




### -param writer [in]


          A pointer to a  <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object on which canonicalization should be stopped.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>
 




## -remarks



<b>WsEndWriterCanonicalization</b> must be called at the same depth at
        which <a href="https://msdn.microsoft.com/e9ea26d6-a136-4103-ac67-42e943ea67b5">WsStartWriterCanonicalization</a> was called.
      


        It is not necessary to call <b>WsEndWriterCanonicalization</b>
        in order to call <a href="https://msdn.microsoft.com/eb1eb835-838a-41e4-9e7d-c5c805237f65">WsFreeWriter</a>.
      



