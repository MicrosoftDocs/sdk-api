---
UID: NC:winfax.PFAX_RECIPIENT_CALLBACKA
title: PFAX_RECIPIENT_CALLBACKA
author: windows-sdk-content
description: The FAX_RECIPIENT_CALLBACK function is an application-defined or library-defined callback function that the FaxSendDocumentForBroadcast function calls to retrieve user-specific information for the transmission.
old-location: fax\_mfax_fax_recipient_callback.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5a5n.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
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
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFAX_RECIPIENT_CALLBACKA callback function


## -description


The <b>FAX_RECIPIENT_CALLBACK</b> function is an application-defined or library-defined callback function that the <a href="https://msdn.microsoft.com/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a> function calls to retrieve user-specific information for the transmission.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a> function.


### -param RecipientNumber [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the number of times the <a href="https://msdn.microsoft.com/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a> function has called the <b>FAX_RECIPIENT_CALLBACK</b> function. Each function call corresponds to one designated fax recipient, and the index is relative to 1.


### -param Context [in]

Type: <b>LPVOID</b>

Pointer to a variable that contains application-specific context information or an application-defined value. <a href="https://msdn.microsoft.com/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a> passes this data to the <b>FAX_RECIPIENT_CALLBACK</b> function.


### -param JobParams [in, out]

Type: <b>PFAX_JOB_PARAM</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structure that contains the information necessary for the fax server to send the fax transmission to the designated recipient. The structure includes, among other items, the recipient's fax number, sender and recipient data, an optional billing code, and job scheduling information. The fax server queues the fax transmission according to the details specified by the <b>FAX_JOB_PARAM</b> structure.


### -param OPTIONAL








#### - CoverpageInfo [in, out, optional]

Type: <b>PFAX_COVERPAGE_INFO</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a> structure that contains cover page data to display on the cover page of the fax document for the designated recipient. This parameter must be <b>NULL</b> if a cover page is not required.


## -returns



Type: <b>BOOL</b>

The function returns a value of nonzero to indicate that the <a href="https://msdn.microsoft.com/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a> function should queue an outbound fax transmission, using the data pointed to by the <i>JobParams</i> and <i>CoverpageInfo</i> parameters.

The function returns a value of zero to indicate that there are no more fax transmission jobs to queue, and calls to <b>FAX_RECIPIENT_CALLBACK</b> should be terminated. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks




<a href="https://msdn.microsoft.com/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a> calls <b>FAX_RECIPIENT_CALLBACK</b> multiple times, once for each designated fax recipient.

The <b>PFAX_RECIPIENT_CALLBACK</b> data type is a pointer to a <b>FAX_RECIPIENT_CALLBACK</b> function.

Call the <a href="https://msdn.microsoft.com/library/ms692819(v=VS.85).aspx">FaxCompleteJobParams</a> function before calling the <b>FAX_RECIPIENT_CALLBACK</b> function. <b>FaxCompleteJobParams</b> is a utility function that fills multiple members in the <a href="https://msdn.microsoft.com/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a> and <a href="https://msdn.microsoft.com/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a> structures, with information such as the sender's name, fax number, and optional billing code information.

A fax client application must specify the <b>FAX_RECIPIENT_CALLBACK</b> function by passing its address when it calls the <a href="https://msdn.microsoft.com/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a> function.

For more information, see <a href="https://msdn.microsoft.com/library/ms691959(v=VS.85).aspx">Transmitting Faxes</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a>



<a href="https://msdn.microsoft.com/library/ms691278(v=VS.85).aspx">FAX_JOB_PARAM</a>



<a href="https://msdn.microsoft.com/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/library/ms690863(v=VS.85).aspx">FaxSendDocumentForBroadcast</a>
 

 

