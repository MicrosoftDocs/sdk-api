---
UID: NC:winfax.PFAX_RECIPIENT_CALLBACKW
title: PFAX_RECIPIENT_CALLBACKW
author: windows-sdk-content
description: The FAX_RECIPIENT_CALLBACK function is an application-defined or library-defined callback function that the FaxSendDocumentForBroadcast function calls to retrieve user-specific information for the transmission.
old-location: fax\_mfax_fax_recipient_callback.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5a5n.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FAX_RECIPIENT_CALLBACK, FAX_RECIPIENT_CALLBACK callback, FAX_RECIPIENT_CALLBACK callback function [Fax Service], PFAX_RECIPIENT_CALLBACKA, PFAX_RECIPIENT_CALLBACKW, _mfax_fax_recipient_callback, fax._mfax_fax_recipient_callback, winfax/FAX_RECIPIENT_CALLBACK, winfax/PFAX_RECIPIENT_CALLBACKA, winfax/PFAX_RECIPIENT_CALLBACKW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PFAX_RECIPIENT_CALLBACKW (Unicode) and PFAX_RECIPIENT_CALLBACKA (ANSI)
req.idl: 
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
 - UserDefined
api_location:
 - Winfax.h
api_name:
 - FAX_RECIPIENT_CALLBACK
 - PFAX_RECIPIENT_CALLBACKA
 - PFAX_RECIPIENT_CALLBACKW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAX_RECIPIENT_CALLBACKW callback function


## -description


The <b>FAX_RECIPIENT_CALLBACK</b> function is an application-defined or library-defined callback function that the <a href="https://msdn.microsoft.com/930c8d2d-4a92-4bb6-8a27-8f4e28207a00">FaxSendDocumentForBroadcast</a> function calls to retrieve user-specific information for the transmission.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param RecipientNumber [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the number of times the <a href="https://msdn.microsoft.com/930c8d2d-4a92-4bb6-8a27-8f4e28207a00">FaxSendDocumentForBroadcast</a> function has called the <b>FAX_RECIPIENT_CALLBACK</b> function. Each function call corresponds to one designated fax recipient, and the index is relative to 1.


### -param Context [in]

Type: <b>LPVOID</b>

Pointer to a variable that contains application-specific context information or an application-defined value. <a href="https://msdn.microsoft.com/930c8d2d-4a92-4bb6-8a27-8f4e28207a00">FaxSendDocumentForBroadcast</a> passes this data to the <b>FAX_RECIPIENT_CALLBACK</b> function.


### -param JobParams [in, out]

Type: <b>PFAX_JOB_PARAM</b>

Pointer to a <a href="https://msdn.microsoft.com/d589a255-abe2-49d5-b593-3a60cdaf61eb">FAX_JOB_PARAM</a> structure that contains the information necessary for the fax server to send the fax transmission to the designated recipient. The structure includes, among other items, the recipient's fax number, sender and recipient data, an optional billing code, and job scheduling information. The fax server queues the fax transmission according to the details specified by the <b>FAX_JOB_PARAM</b> structure.


### -param CoverpageInfo [in, out, optional]

Type: <b>PFAX_COVERPAGE_INFO</b>

Pointer to a <a href="https://msdn.microsoft.com/488a4c89-7efc-4aa5-aa8d-b6cc2ccd2535">FAX_COVERPAGE_INFO</a> structure that contains cover page data to display on the cover page of the fax document for the designated recipient. This parameter must be <b>NULL</b> if a cover page is not required.


## -returns



Type: <b>BOOL</b>

The function returns a value of nonzero to indicate that the <a href="https://msdn.microsoft.com/930c8d2d-4a92-4bb6-8a27-8f4e28207a00">FaxSendDocumentForBroadcast</a> function should queue an outbound fax transmission, using the data pointed to by the <i>JobParams</i> and <i>CoverpageInfo</i> parameters.

The function returns a value of zero to indicate that there are no more fax transmission jobs to queue, and calls to <b>FAX_RECIPIENT_CALLBACK</b> should be terminated. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks




<a href="https://msdn.microsoft.com/930c8d2d-4a92-4bb6-8a27-8f4e28207a00">FaxSendDocumentForBroadcast</a> calls <b>FAX_RECIPIENT_CALLBACK</b> multiple times, once for each designated fax recipient.

The <b>PFAX_RECIPIENT_CALLBACK</b> data type is a pointer to a <b>FAX_RECIPIENT_CALLBACK</b> function.

Call the <a href="https://msdn.microsoft.com/46eb9960-1d07-4792-83d6-d2f5948e05e9">FaxCompleteJobParams</a> function before calling the <b>FAX_RECIPIENT_CALLBACK</b> function. <b>FaxCompleteJobParams</b> is a utility function that fills multiple members in the <a href="https://msdn.microsoft.com/488a4c89-7efc-4aa5-aa8d-b6cc2ccd2535">FAX_COVERPAGE_INFO</a> and <a href="https://msdn.microsoft.com/d589a255-abe2-49d5-b593-3a60cdaf61eb">FAX_JOB_PARAM</a> structures, with information such as the sender's name, fax number, and optional billing code information.

A fax client application must specify the <b>FAX_RECIPIENT_CALLBACK</b> function by passing its address when it calls the <a href="https://msdn.microsoft.com/930c8d2d-4a92-4bb6-8a27-8f4e28207a00">FaxSendDocumentForBroadcast</a> function.

For more information, see <a href="https://msdn.microsoft.com/bee4d50b-d6e3-432b-9db6-c7df837079f4">Transmitting Faxes</a>.




## -see-also




<a href="https://msdn.microsoft.com/488a4c89-7efc-4aa5-aa8d-b6cc2ccd2535">FAX_COVERPAGE_INFO</a>



<a href="https://msdn.microsoft.com/d589a255-abe2-49d5-b593-3a60cdaf61eb">FAX_JOB_PARAM</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/930c8d2d-4a92-4bb6-8a27-8f4e28207a00">FaxSendDocumentForBroadcast</a>
 

 

