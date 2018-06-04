---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# MAPISENDMAIL callback function


## -description


<p class="CCE_Message">[<b>MAPISendMail</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a>.
]

Sends an ANSI message.

<b>On Windows 8 and later:  </b>Call <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a> to send a message.

<b>On Windows 7 and earlier:  </b>Use <a href="https://msdn.microsoft.com/3FBE0950-6D73-4130-9F17-F1449247AB0F">MAPISendMailHelper</a> to send a message.


## -parameters




### -param lhSession [in]

Type: <b>LHANDLE</b>

For more information, see the <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a> function.


### -param ulUIParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG_PTR</a></b>

For more information, see the <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a> function.


### -param lpMessage [in]

Type: <b><a href="https://msdn.microsoft.com/7f696dd6-bfae-4c7d-b55f-d37952691c02">lpMapiMessage</a></b>

For more information, see the <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a> function.


### -param flFlags [in]

Type: <b>FLAGS</b>

For more information, see the <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a> function.


### -param ulReserved

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

For more information, see the <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a> function.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

For more information, see the <a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a> function.




## -see-also




<a href="https://msdn.microsoft.com/5a61f0f2-347e-40fb-b7f9-6b42690cbcd8">MAPILogon</a>



<a href="https://msdn.microsoft.com/79a2f17e-fb07-4f3b-b8f6-0448399ffa50">MAPISendDocuments</a>



<a href="https://msdn.microsoft.com/3FBE0950-6D73-4130-9F17-F1449247AB0F">MAPISendMailHelper</a>



<a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a>



<a href="https://msdn.microsoft.com/7f696dd6-bfae-4c7d-b55f-d37952691c02">MapiMessage</a>



<a href="https://msdn.microsoft.com/1457617f-de55-4875-91f5-afddee84b782">MapiRecipDesc</a>



<a href="https://msdn.microsoft.com/a8330f38-3ef0-4b36-a5e7-89837088cbef">Simple MAPI</a>
 

 

