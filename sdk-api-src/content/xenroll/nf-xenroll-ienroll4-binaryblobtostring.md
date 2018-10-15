---
UID: NF:xenroll.IEnroll4.binaryBlobToString
title: IEnroll4::binaryBlobToString
author: windows-sdk-content
description: Converts a binary data BLOB to a string. This method uses the CryptBinaryToString function to perform the conversion. This method was first defined in the IEnroll4 interface.
old-location: security\ienroll4_binaryblobtostring.htm
tech.root: seccrypto
ms.assetid: 0ce10b31-29f4-4fda-a488-7bc124e9461e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IEnroll4 interface [Security],binaryBlobToString method, IEnroll4.binaryBlobToString, IEnroll4::binaryBlobToString, binaryBlobToString, binaryBlobToString method [Security], binaryBlobToString method [Security],IEnroll4 interface, security.ienroll4_binaryblobtostring, xenroll/IEnroll4::binaryBlobToString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.binaryBlobToString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll4::binaryBlobToString


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>binaryBlobToString</b> method converts a binary data <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> to a string. This method uses the 
<a href="https://msdn.microsoft.com/e6bdf931-fba3-4a33-b22e-5f818f565842">CryptBinaryToString</a> function to perform the conversion. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param Flags [in]

Value passed to the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/e6bdf931-fba3-4a33-b22e-5f818f565842">CryptBinaryToString</a> function. For a description of possible values, see 
<a href="https://msdn.microsoft.com/e6bdf931-fba3-4a33-b22e-5f818f565842">CryptBinaryToString</a>.


### -param pblobBinary [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> that represents the binary BLOB to  convert to a string.


### -param ppwszString [out]

A pointer to a <b>LPWSTR</b> that receives the encoded data.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

