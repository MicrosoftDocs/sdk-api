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

# IWSManEx::GetErrorMessage


## -description


Returns a formatted string containing the text of an error number. This method performs the same operation as the <b>Winrm</b> command-line <b>winrm helpmsg </b><i>error number</i>. 


## -parameters




### -param errorNumber [in]

Error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.


### -param errorMessage [out]

Error message string formatted like messages returned from the  <b>Winrm</b> command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The corresponding scripting method is <a href="https://msdn.microsoft.com/5f0a5259-8356-4406-8612-34f4921184f0">WSMan.GetErrorMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a>
 

 

