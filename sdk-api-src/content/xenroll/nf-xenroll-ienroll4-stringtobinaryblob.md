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

# IEnroll4::stringToBinaryBlob


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>stringToBinaryBlob</b> method converts an encoded string to a binary data <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.

The <b>stringToBinaryBlob</b> method calls the 
<a href="https://msdn.microsoft.com/13b6f5ef-174a-4254-8492-6e7dcc58945f">CryptStringToBinary</a> function. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param Flags [in]

Value passed to the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/13b6f5ef-174a-4254-8492-6e7dcc58945f">CryptStringToBinary</a> function. For valid values, see 
<a href="https://msdn.microsoft.com/13b6f5ef-174a-4254-8492-6e7dcc58945f">CryptStringToBinary</a> .


### -param pwszString [in]

Encoded string to be converted to a binary data BLOB.


### -param pblobBinary [out]

A pointer to a  <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that receives the binary data.


### -param pdwSkip [out]

A pointer to <b>LONG</b> that receives the number of characters in any skipped strings up to the beginning of actual base64 or hexadecimal strings.


### -param pdwFlags [out]

A pointer to <b>LONG</b> that receives the actual format used in the conversion


## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

